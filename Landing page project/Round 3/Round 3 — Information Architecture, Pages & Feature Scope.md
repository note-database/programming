
**دو Demo ما نباید دو محصول جدا باشند.**  
هر دو باید روی یک معماری، Design System و Component Language مشترک ساخته شوند و فقط Art Direction، Hero composition، بعضی Layoutها و محتوای Persona متفاوت باشد. اگر هر Demo ساختار خودش را داشته باشد، هزینه توسعه و QA تقریباً دو برابر می‌شود.

حالا سؤال‌ها:

1. **Homepage تا چه اندازه کامل باشد؟**  
    سه مدل منطقی داریم: Homepage فقط معرفی کوتاه و لینک به صفحات داخلی؛ Homepage تقریباً کامل و صفحات داخلی برای جزئیات؛ یا Homepage کاملاً One-page و صفحات داخلی صرفاً Project/Blog.  
    **پیشنهاد من: مدل دوم، ولی نزدیک به سوم.** Home باید به‌تنهایی یک Personal Website کامل باشد، اما جزئیات سنگین مثل Case Study و Blog Detail وارد صفحات مستقل شوند. ساختار پیشنهادی:  
    `Hero → About → Skills/Expertise → Experience → Featured Projects → Clients(optional) → Blog Preview → Contact/CTA → Footer`.  
    دلیل: خریدار اگر فقط `index.html` را شخصی‌سازی کند، باید سایت قابل استفاده داشته باشد.
    
2. **آیا About صفحه مستقل داشته باشد؟**  
    **پیشنهاد من: در v1 نه.** About کامل داخل Homepage باشد. صفحه مستقل About ارزش زیادی اضافه نمی‌کند و فقط محتوا را تکراری می‌کند. اگر بعدها محصول رشد کرد می‌تواند اضافه شود.
    
3. **آیا Resume صفحه مستقل داشته باشد؟**  
    پیشنهاد من باز هم **نه در v1**. Resume باید یک Section قوی داخل Homepage باشد. کاربر می‌تواند PDF رزومه خودش را هم لینک کند. صفحه Resume جدا در این مرحله بیشتر حجم محصول را زیاد می‌کند تا ارزش آن را.
    
4. **Portfolio صفحه مستقل داشته باشد؟**  
    **پیشنهاد من: حتماً بله.** Homepage فقط Featured Projects را نشان دهد؛ مثلاً 4 تا 6 پروژه منتخب. صفحه `portfolio.html` همه پروژه‌ها، دسته‌بندی و Filtering را نمایش دهد. این تصمیم Portfolio را واقعاً به مرکز محصول تبدیل می‌کند.
    
5. **Project Detail چند Template داشته باشد؟**  
    وسوسه ساخت چند مدل زیاد است. من پیشنهاد می‌کنم در `v1.0` فقط **یک Case Study Template فوق‌العاده قوی** داشته باشیم. تفاوت پروژه‌ها با محتوا، Gallery و Media ایجاد شود، نه با 5 فایل HTML تقریباً تکراری. اگر بعداً Feedback نشان داد نیاز هست، Variation اضافه می‌کنیم.
    
6. **ساختار Case Study دقیقاً چه باشد؟**  
    پیشنهاد من این Scope است:  
    `Project Hero → Overview → Metadata → Challenge → Role/Responsibilities → Process → Solution → Visual Gallery → Results/Outcome → Tools/Technologies → External Link → Previous/Next Project`.  
    یک نکته مهم: `Results` باید Optional باشد، چون همه کاربران عدد و KPI ندارند. حذفش نباید Layout را خراب کند.
    
7. **Portfolio Grid چه نوع پروژه‌هایی را پشتیبانی کند؟**  
    پیشنهاد من حداقل این مدل‌ها: Web, UI/UX, Branding/Creative, App. اما این Categoryها فقط Demo Content باشند؛ ساختار باید طوری باشد که خریدار نام دسته‌ها را آزادانه عوض کند. یعنی JS نباید به واژه‌های ثابت `web` یا `design` وابسته باشد.
    
8. **Filtering چطور پیاده شود؟**  
    همان تصمیم قبلی را دقیق‌تر می‌کنم: Vanilla JS، Progressive Enhancement. حتی اگر JavaScript غیرفعال باشد، همه پروژه‌ها باید دیده شوند؛ فقط Filter از کار بیفتد. این استاندارد مهم است و از JS شکننده جلوگیری می‌کند.
    
9. **آیا Portfolio Search داشته باشیم؟**  
    **پیشنهاد من: نه.** برای یک Personal Portfolio با 6 تا 15 پروژه، Search مصنوعی و بی‌ارزش است. Category Filter کافی است. این Feature را وارد Scope نکنیم.
    
10. **Blog در Homepage چقدر دیده شود؟**  
    پیشنهاد من فقط **3 مقاله آخر** با Cardهای تمیز. Homepage نباید تبدیل به News Website شود. دکمه `View all articles` کاربر را به `blog.html` ببرد.
    
11. **Blog List چقدر پیچیده باشد؟**  
    پیشنهاد من: Grid/List ساده با Category Label، Date، Reading Time، Image و Excerpt.  
    در `v1` این‌ها را نمی‌خواهم: Search، Pagination پیچیده، Tag archive، Category archive، Sidebar شلوغ، Newsletter system. اینها برای یک HTML Portfolio بیش از حد هستند.
    
12. **Blog Detail چه امکاناتی داشته باشد؟**  
    پیشنهاد من:  
    `Title → Meta → Cover → Article Content → Headings → Blockquote → Inline Image → Lists → Code Block → Share Links(optional) → Author snippet → Previous/Next Article`.  
    چون مخاطب ما Developer هم هست، **Code Block styling** ارزشمند است. Comments را وارد v1 نمی‌کنیم.
    
13. **Hero چه میزان اطلاعات داشته باشد؟**  
    پیشنهاد من Hero را شلوغ نکنیم. باید شامل:  
    `Name / Role / concise positioning statement / primary CTA / secondary CTA / portrait or visual identity / social links`.  
    Skills logo، statistics، clients، GitHub و ده چیز دیگر نباید همزمان داخل Hero باشند. Hero باید Identity بسازد نه Inventory.
    
14. **CTA اصلی Homepage چه باشد؟**  
    پیشنهاد من برای Demo Developer: `View My Work`.  
    CTA ثانویه: `Download CV` یا `Contact Me`.  
    برای Designer هم Primary CTA همچنان Portfolio-first باشد. دلیل: Positioning اصلی محصول ما «نمایش حرفه‌ای کار» است، نه صرفاً تماس گرفتن.
    
15. **About Section چقدر طولانی باشد؟**  
    پیشنهاد من: Intro کوتاه + اطلاعات اصلی + چند Fact/Metric. نه Biography چند پاراگرافی طولانی. چیزی در حد:  
    `Short bio / location / availability / years experience / selected facts / CV CTA`.  
    Long-form biography می‌تواند در آینده اضافه شود، ولی برای v1 لازم نیست.
    
16. **Skills را با Progress Bar نمایش دهیم؟**  
    من **Progress Barهای 90% HTML / 80% JS را توصیه نمی‌کنم.** این Pattern قدیمی و از نظر معنایی ضعیف است.  
    پیشنهاد من: Skill Groups + Tools + proficiency wording در صورت نیاز. مثلاً `Frontend`, `Design Tools`, `Workflow`. اگر درصد لازم شد فقط در یکی از Demoها و به شکل محدود، نه هسته اصلی UI.
    
17. **Experience و Education چه Layoutی داشته باشند؟**  
    پیشنهاد من: Timeline مدرن ولی ساده. هر Item:  
    `Date / Role or Degree / Organization / Short description / optional location`.  
    Animation سنگین روی Timeline نمی‌خواهیم. خوانایی از نمایشی بودن مهم‌تر است.
    
18. **Awards و Certificates دقیقاً چطور Optional باشند؟**  
    پیشنهاد من آنها را داخل Resume Section به‌عنوان **Submodule جدا** طراحی کنیم، نه Section مستقل Homepage. یعنی اگر کاربر نیاز داشت فعال می‌کند؛ اگر حذف کرد spacing و hierarchy تمیز باقی می‌ماند.
    
19. **GitHub Featured Repositories کجا باشد؟**  
    پیشنهاد من آن را برای Demo Developer به شکل یک Subsection بعد از Projects یا داخل About/Expertise نگذاریم. بهترین جای آن بعد از Featured Projects است، چون ابتدا باید کارهای بصری/Case Study دیده شوند و بعد Repositoryها نقش Evidence فنی را بازی کنند. برای Demo Designer همان Block اصلاً نمایش داده نشود.
    
20. **Client Logos کجا قرار بگیرند؟**  
    چون Optional هستند، پیشنهاد من یک Strip یا Grid بسیار جمع‌وجور بعد از About یا Projects است. نه Carousel اجباری. Static grid از نظر performance و accessibility بهتر است. اگر مشتری هیچ Clientی ندارد، کل Section حذف شود.
    
21. **Testimonials را که از v1 حذف کردیم، آیا جای خالی برایش از الان طراحی کنیم؟**  
    **پیشنهاد من: نه.** نباید در معماری فعلی برای Feature آینده حفره بسازیم. وقتی در Update اضافه شد، براساس Feedback جای درستش را تعیین می‌کنیم. Future-proofing زیاد خودش شکل دیگری از Overengineering است.
    
22. **Services و Pricing هم همین وضعیت را داشته باشند؟**  
    بله. هیچ Placeholder، Comment بزرگ یا CSS unused برایشان در v1 نگه نمی‌داریم. Backlog یعنی «خارج از کد فعلی».
    
23. **Contact Section چه داشته باشد؟**  
    چون Form فعلاً UI-only است، پیشنهاد من:  
    `Name / Email / Subject / Message / Submit button + email / location(optional) / social links`.  
    اما در UI و Documentation باید کاملاً واضح باشد که ارسال واقعی Backend ندارد. نباید مشتری فکر کند Form کار می‌کند در حالی که فقط ظاهر است.
    
24. **آیا Map داشته باشیم؟**  
    پیشنهاد من **نه در v1**. Google Maps/API dependency برای Personal Portfolio ارزش کافی ندارد و Privacy/Performance را هم پیچیده می‌کند. Address یا Location text کافی است.
    
25. **آیا Social Links در چند جای سایت تکرار شوند؟**  
    پیشنهاد من حداکثر در Hero و Footer/Contact. اگر Navbar، Hero، About، Contact و Footer همگی 6 Icon تکراری داشته باشند، UI شلوغ می‌شود.
    
26. **Navigation چگونه باشد؟**  
    برای معماری Hybrid پیشنهاد من Navigation اصلی:  
    `Home / About / Resume / Portfolio / Blog / Contact`.  
    در Homepage اینها Anchor باشند؛ `Portfolio` و `Blog` علاوه بر Anchor preview، صفحه مستقل هم داشته باشند. باید از UX مبهمی که یک آیتم گاهی Scroll می‌کند و گاهی صفحه عوض می‌کند اجتناب کنیم؛ در Round UX دقیقاً interaction آن را تعیین می‌کنیم.
    
27. **آیا Navbar باید CTA داشته باشد؟**  
    پیشنهاد من یک CTA کوچک مثل `Let's Talk` یا `Hire Me` فقط در Desktop، ولی نه در تمام حالات. برای Portfolio personal مناسب است، اما باید Secondary باشد و Projects همچنان Primary focus بماند.
    
28. **Footer چقدر کامل باشد؟**  
    پیشنهاد من Footer سبک:  
    `Name/brand + short line + navigation shortcuts + social links + copyright`.  
    Newsletter، چند ستون Link و Footer شبیه SaaS نمی‌خواهیم.
    
29. **404 Page داشته باشیم؟**  
    **بله.** یک `404.html` ساده ولی کاملاً هماهنگ با Design System. هزینه کم، کیفیت Packaging بالا. این یکی از Featureهایی است که واقعاً ارزش دارد.
    
30. **آیا Coming Soon / Maintenance Page داشته باشیم؟**  
    **پیشنهاد من: نه در v1.** محصول Portfolio است، نه multipurpose pack. اگر بعدها درخواست شد اضافه می‌کنیم.
    
31. **آیا Preloader داشته باشیم؟**  
    پیشنهاد من **به‌صورت پیش‌فرض نه**. اگر Art Direction یکی از Demoها نیاز داشت، فقط یک transition بسیار کوتاه و قابل غیرفعال‌کردن. Preloaderهای نمایشی اغلب مشکل Performance را پنهان می‌کنند.
    
32. **آیا Back-to-top داشته باشیم؟**  
    پیشنهاد من بله، ولی فقط وقتی صفحه به‌اندازه کافی Scroll شده است. کوچک، accessible و بدون animation اغراق‌شده.
    
33. **آیا Custom Cursor داشته باشیم؟**  
    پیشنهاد من **نه برای Core**. این یکی از چیزهایی است که قالب را سریع «Template-y» می‌کند و روی touch device هم معنایی ندارد. اگر بعدها یک Demo Experimental ساختیم شاید Optional شود.
    
34. **آیا Page Transition بین صفحات داشته باشیم؟**  
    پیشنهاد من خیلی محدود. Fade/translate کوتاه در صورت امکان بدون جلوگیری از Navigation واقعی. هیچ Router مصنوعی با AJAX نمی‌خواهیم. Template باید لینک‌های استاندارد HTML داشته باشد.
    
35. **آیا Smooth Scroll داشته باشیم؟**  
    بله، ولی با CSS/JS سبک و رعایت `prefers-reduced-motion`. اگر کاربر Reduced Motion دارد، animation باید حذف شود.
    
36. **آیا Statistics / Fun Facts داشته باشیم؟**  
    مثل `5+ Years / 40 Projects / 20 Clients`.  
    پیشنهاد من به‌عنوان Optional micro-block داخل About، نه Section مستقل. Counter animation هم ضروری نیست.
    
37. **آیا “Availability for Work” Indicator داشته باشیم؟**  
    من این را برای Demo Developer/Designer بسیار مناسب می‌دانم. مثلاً یک Badge کوچک `Available for freelance`. اما باید راحت حذف شود. Feature کوچک است ولی Personal Branding را قوی می‌کند.
    
38. **آیا Download CV واقعی در Demo قرار دهیم؟**  
    بله. داخل Package یک PDF placeholder/نمونه سبک یا فایل راهنما می‌تواند وجود داشته باشد، ولی خود Documentation باید بگوید کاربر فایل خودش را جایگزین کند. CV CTA شکسته در Demo غیرقابل قبول است.
    
39. **آیا تصاویر Demo باید کاملاً متفاوت برای RTL و LTR باشند؟**  
    پیشنهاد من محتوا و تصاویر Persona در نسخه‌های RTL/LTR تا حدی یکسان باشند تا QA و Maintenance ساده بماند؛ اما متن و composition باید برای هر Direction طبیعی شود. هدف «ترجمه مکانیکی» نیست.
    
40. **دو Demo دقیقاً چه تفاوتی داشته باشند؟**  
    پیشنهاد اولیه من:
    
    - **Demo 01 — Creative Developer:** ساختار کمی Technical‌تر، Featured Repositories، dark-first یا balanced، geometry و motion کمی بیشتر.
    - **Demo 02 — Digital Designer:** imagery بزرگ‌تر، editorial composition، case-study-first، light-first یا visually softer.
    
    اما هر دو باید همان Pages، همان Case Study engine و همان Core Design System را به اشتراک بگذارند.
    

---

## Scope پیشنهادی من برای `v1.0`

اگر بخواهم همین الان یک Scope تمیز و قابل دفاع بسازم، این است:

```
index.html
portfolio.html
project-details.html
blog.html
blog-details.html
404.html
```

برای Demo دوم به‌جای تکثیر بی‌حساب صفحات، فقط Variationهای ضروری را اضافه می‌کنیم؛ مثلاً `index-2.html` و اگر واقعاً Layout داخلی متفاوت بود Variation محدود مرتبط.

Core Sections:

```
Hero
About
Skills / Expertise
Experience + Education
Awards / Certificates (optional module)
Featured Projects
Static GitHub Repositories (Developer demo only)
Client Logos (optional)
Blog Preview
Contact
Footer
```

Core Features:

```
RTL + LTR
Light + Dark + System preference
Responsive design
Accessible navigation
Portfolio filtering
Case Study page
Blog list/detail
Design tokens
Reduced-motion support
Easy section removal
Static contact UI
Back-to-top
CV download
SEO-ready markup
```

**خارج از `v1.0`:**

```
Testimonials
Services
Pricing
PHP/AJAX contact
Map
Comments
Blog search
Portfolio search
Multiple case-study layouts
Custom cursor
Heavy page transitions
WebGL / 3D
Music
Admin panel
CMS
API integrations
Complex animations
Coming soon page
```

این Scope به‌نظر من **به‌اندازه کافی بزرگ هست که Premium دیده شود، ولی هنوز آن‌قدر کوچک هست که بتوانیم واقعاً روی کیفیت تک‌تک بخش‌ها وسواس داشته باشیم.**

### فقط به این 4 تصمیم حتماً جواب بده

بقیه پیشنهادهای این Round را اگر تأیید می‌کنی لازم نیست یکی‌یکی تکرار کنی. فقط این چهار مورد تصمیم طراحی واقعی می‌خواهند:

**A)** ساختار Homepage پیشنهادی من را تأیید می‌کنی؟  
**B)** `About` و `Resume` در v1 صفحه مستقل نداشته باشند؟  
**C)** Scope فایل‌های اصلی `index / portfolio / project-details / blog / blog-details / 404` را تأیید می‌کنی؟  
**D)** تفاوت دو Demo را روی `Creative Developer` و `Digital Designer` با معماری مشترک تأیید می‌کنی؟

اگر این چهار مورد را تأیید کنی، **Round 3 را قفل می‌کنیم و بعد می‌رویم سراغ مهم‌ترین بخش برای چیزی که از اول رویش تأکید داشتی: Round 4 — UI/UX Art Direction**؛ آنجا درباره Layout composition، grid، typography، visual hierarchy، shape language، imagery، hero architecture، color philosophy، density، navigation style و شخصیت بصری محصول با جزئیات خیلی بیشتر تصمیم می‌گیریم.