# PKG Sender Android — handoff (2026-09-22)

## وضعیت: منطق کامل است، فقط ظاهر مانده

### چه چیزهایی تمام شده (droid1 تا droid24)
- ارسال مستقیم PKG به PS5/PS4 بدون کپی (SAF seek + `IRangeSource`)، resume/range کامل
- ارسال image ‏(exfat/ffpfsc/ffpkg/pfs)‏ با pull به `/data/homebrew` + resume خودکار تا ۶ بار
- کاور PKG و exfat از روی خود فایل؛ `icon_url` یکتا برای نوتیف کنسول
- دکمه Test: پروب کنسول، IP وای‌فای گوشی، سلف‌تست سرور، diagnose تک‌تک پورت‌ها
- کش fresh (بدون stale offline)، قفل Wi-Fi/Wake ضد قطع شدن، لاگ داخل‌برنامه + لاگ فایل ماندگار + شکارچی کرش
- فیکس OOM (بافر reuse، largeHeap)
- کاور ffpfsc/ffpkg روی گوشی ممکن نیست (کانتینر فشرده/UFS — نیاز به پورت mkpfs/pytsk3)

### چه مانده (سشن بعد)
- فقط UI: نمونه SlipNet (Material3 داینامیک) — دکمه‌ها، نوار، کادرها تم اندروید بگیرند
- وضعیت فعلی droid24 از قبل Material3 است (تولبار، کارت، فیلد outlined، bottom-sheet) ولی باید دقیق‌تر مثل نمونه بشود

### نکته‌ها
- ریلیز نزن (فقط پوش + APK در تلگرام)
- APKها در روت ریپو untracked هستند (droid*.apk) — کامیت نمی‌شوند
- بیلد: `D:\OpenCode\.dotnet\dotnet.exe publish -c Release -p:AndroidSdkDirectory=%LOCALAPPDATA%\Android\Sdk` در `droid/`
