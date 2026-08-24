خیلی خوب. الان اطلاعات کافی داریم که از مرحله «ایده مبهم» عبور کنیم و وارد **Product Definition واقعی** شویم.

بعد از بررسی جواب‌هایت و بازار فعلی راست‌چین، چند تصمیم را باید همین‌جا اصلاح کنم؛ چون اگر همه انتخاب‌هایت را بدون نقد وارد Master Prompt کنیم، یک پرامپت بزرگ ولی متناقض خواهیم داشت.

## نتیجه اصلی تحقیق بازار

من فعلاً پیشنهاد می‌کنم محصول اولت را از «Landing Page عمومی» به این تبدیل کنیم:

> **Premium Persian Developer / Freelancer Personal Portfolio HTML Template**

یعنی یک قالب شخصی/رزومه/نمونه‌کار برای **برنامه‌نویس، طراح، فریلنسر و متخصص دیجیتال ایرانی**.

چرا؟

دسته HTML شخصی راست‌چین در حال حاضر حدود ۱۳۸ محصول دارد و نمونه‌های موفق واقعی در آن وجود دارند: Tokyo بیش از ۴۰۰ فروش، Procard حدود ۲۹۶ فروش، Kyros حدود ۷۴ فروش و چند قالب تک‌صفحه‌ای نیز به محدوده ۵۰ فروش رسیده‌اند. بنابراین هدف تو یعنی **حداقل ۵۰ فروش، از نظر سابقه بازار غیرواقعی نیست**. [راست چین](https://www.rtl-theme.com/category/template-html/personal-html/)

در مقابل، صفحه فعلی Landing HTML تعداد زیادی محصول جدید با ۰ تا چند فروش دارد؛ هرچند استثناهای موفقی مثل APPER با بیش از ۱۵۰ فروش و Limty با بیش از ۶۰ فروش هم وجود دارند. بنابراین «صرفاً یک لندینگ زیبا» برای من thesis تجاری ضعیف‌تری است. [راست چین](https://www.rtl-theme.com/category/template-html/html-landing-page/)

اما نکته جالب‌تر اینجاست: Tokyo با همان چیزهایی فروخته که تو دنبالش هستی؛ مینیمال، نسخه تاریک/روشن، responsive، نسخه انگلیسی، SEO، مستندات و ساختار توسعه‌پذیر. در نتیجه این موارد **دیگر مزیت رقابتی نیستند؛ baseline بازارند.** [راست چین](https://www.rtl-theme.com/tokyo-html-template/)

این تمایز بسیار مهم است.

---

# چند مورد از جواب‌هایت که باید اصلاح کنیم

### 1. «Responsive بودن» مزیت رقابتی نیست

این جمله:

> چرا مشتری محصول من را بخرد؟ چون بسیار دقیق responsive است.

برای صفحه فروش خوب است، ولی **دلیل خرید نیست**.

Responsive، clean code، SEO، documentation و عدم وجود console error چیزهایی هستند که محصول حرفه‌ای باید به‌طور پیش‌فرض داشته باشد.

تمایز باید چیزی باشد که مشتری در Screenshot اول ببیند یا فوراً در Demo تجربه کند.

بنابراین تمایز اصلی محصول ما را روی این سه محور می‌گذارم:

**Design differentiation + Iranian developer-specific UX + exceptional customization**

نه صرفاً «کدنویسی تمیز».

---

# 2. درباره ۲۰ فونت فارسی پولی: این را فعلاً رد می‌کنم

این قسمت خطرناک است:

> ۲۰ تا فونت فارسی پولی داخل قالب.

اگر مجوز فونت اجازه **redistribution داخل محصول تجاری قابل فروش** را ندهد، نمی‌توانیم فایل‌ها را همراه قالب منتشر کنیم.

خرید یک فونت برای استفاده شخصی/وب‌سایت لزوماً به معنی حق قرار دادن فایل فونت داخل محصولی که صدها نفر دانلود می‌کنند نیست.

بنابراین در Master Prompt قرار می‌دهیم:

> **No asset may be redistributed unless its license explicitly permits redistribution inside a commercial template product.**

در v1 بهتر است یک فونت اصلی قانونی و قابل توزیع داشته باشیم و Documentation توضیح دهد مشتری چطور فونت خودش را جایگزین کند.

این خیلی حرفه‌ای‌تر از «۲۰ فونت» است.

---

# 3. Tailwind را برای این محصول پیشنهاد نمی‌کنم

با اینکه Tailwind v4 ابزار خوبی است، برای **این محصول مشخص** پیشنهاد من:

**HTML5 + modular vanilla CSS + Vanilla JavaScript ES Modules**

است.

دلیلش این است که خریدار قالب HTML معمولاً انتظار دارد:

```
index.html
assets/css/
assets/js/
assets/images/
```

را ببیند و خیلی راحت تغییرش دهد.

Tailwind مزیت مهمی برای **تو به عنوان توسعه‌دهنده** ایجاد می‌کند، ولی الزاماً برای **خریدار قالب HTML** مزیت ایجاد نمی‌کند.

از طرف دیگر تو BEM، CSS modular، CSS Variables و customization ساده می‌خواهی. Vanilla CSS اینجا خیلی تمیز با همه‌شان جور درمی‌آید.

بنابراین پیشنهاد:

```
HTML5
CSS3
BEM
CSS Custom Properties
Vanilla JavaScript
ES Modules
Vite for development/build
```

و:

```
Bootstrap ❌
Tailwind ❌
SCSS ❌
jQuery ❌
```

برای محصول اول، این stack بسیار کنترل‌شده‌تر است.

---

# 4. Desktop-first را هم رد می‌کنم

تو گفتی:

> desktop-first ولی موبایل مهم‌تر باشد.

این دو تصمیم از لحاظ مهندسی با هم هم‌جهت نیستند.

اگر Mobile برایمان اهمیت ویژه دارد، بهتر است:

> **Mobile-first CSS + progressive enhancement**

داشته باشیم.

یعنی طراحی را می‌توانیم ابتدا Desktop در Figma/تصور بصری بررسی کنیم، ولی **CSS architecture را mobile-first** می‌نویسیم.

مثلاً:

```
.project-grid {
  grid-template-columns: 1fr;
}

@media (min-width: 768px) {
  .project-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
```

نه برعکس.

در Master Prompt همین را قرار می‌دهم.

---

# 5. BEM برای ID اشتباه است

گفتی:

> همه کلاس‌ها و IDها BEM باشند.

BEM برای **class naming** است، نه اینکه ID هم با BEM مدیریت شود.

قرار ما:

```
Classes → BEM
IDs → فقط برای semantic hooks / anchor targets / JS hooks در صورت ضرورت
```

حتی برای JavaScript بهتر است از:

```
data-js="mobile-menu"
```

استفاده کنیم تا behavior را از styling جدا کنیم.

این تصمیم کیفیت معماری را بالا می‌برد.

---

# 6. JavaScript: تصمیم من

برای این پروژه:

**Vanilla JavaScript + ES Modules + functional/module-based architecture**

نه Class-heavy architecture.

مثلاً:

```
theme.js
navigation.js
accordion.js
portfolio-filter.js
contact-form.js
animations.js
```

Classes فقط اگر واقعاً stateful component پیچیده داشته باشیم.

jQuery:

**کاملاً ممنوع.**

---

# 7. Dependency Policy

من نمی‌خواهم محصول اول تبدیل شود به:

```
GSAP
AOS
Swiper
jQuery
Bootstrap
Icon Library
...
```

فقط برای اینکه حرفه‌ای به نظر برسد.

قانون:

> **Zero dependency by default. Every dependency must earn its place.**

برای animationهای معمولی:

```
CSS
IntersectionObserver
Web Animations API
```

کافی هستند.

Swiper فقط اگر واقعاً carousel پیچیده داشته باشیم.

GSAP فقط اگر Design Concept واقعاً بدون آن قابل اجرا نباشد.

AOS را نمی‌خواهم.

jQuery را نمی‌خواهم.

Iconها:

**SVG sprite / local SVG**

بهتر است.

---

# 8. Dark Mode قرار نیست «نسخه سیاه سایت» باشد

اینجا کاملاً با خواسته‌ات موافقم.

قرار نیست:

```
background: #000;
color: #fff;
```

بزنیم و اسمش را Dark Theme بگذاریم.

دو Theme باید **دو Art Direction مرتبط** باشند.

مثلاً:

### Light

```
Warm off-white
graphite
soft violet accent
subtle borders
paper-like surfaces
```

### Dark

```
deep graphite/navy
muted luminous accent
layered surfaces
subtle ambient glow
controlled contrast
```

اما Layout و component system یکی باقی می‌مانند.

این می‌تواند واقعاً یکی از نقاط قوت محصول شود.

---

# 9. Accessibility را کامل وارد محصول می‌کنم

تمام مواردی که درباره‌شان مطمئن نبودی را من این‌طور تعیین می‌کنم:

- Semantic HTML
- Keyboard navigation
- Visible focus
- صحیح بودن labelهای فرم
- ARIA فقط در صورت نیاز
- Skip-to-content
- Color contrast مناسب
- `prefers-reduced-motion`
- Accessible mobile navigation
- Accessible accordion
- Accessible theme switch
- Accessible language switch
- Alt text strategy

Accessibility را شاید تیتر اصلی تبلیغاتی محصول نکنیم، ولی **Release Requirement** خواهد بود.

---

# 10. Performance target

هدف اولیه:

```
Performance >= 90
Accessibility >= 95
Best Practices >= 95
SEO >= 95
```

ولی یک اشتباه را هم اصلاح کنم:

> «JavaScript را محدود نکن چون نمی‌خواهم کیفیت فدای کمیت شود.»

حجم بیشتر JavaScript معمولاً کیفیت بیشتر نیست.

برعکس:

> **کمترین JavaScript لازم برای بهترین تجربه.**

این اصل پروژه خواهد بود.

---

# 11. SEO

همه این‌ها را وارد می‌کنیم:

```
Semantic heading hierarchy
unique title
meta description
canonical
Open Graph
Twitter/X metadata
favicon
robots.txt
sitemap.xml
structured data
image dimensions
alt attributes
crawlable links
clean HTML
```

برای portfolio می‌توانیم Schemaهایی مثل `Person` و در جاهای لازم `CreativeWork`/`WebSite` را بررسی کنیم.

---

# 12. Browser Support

پیشنهاد:

```
Chrome latest 2
Firefox latest 2
Edge latest 2
Safari latest 2
Safari iOS latest 2
Chrome Android current
```

IE را پشتیبانی نمی‌کنیم.

---

# 13. QA باید سخت‌گیرانه باشد

تمام موارد بخش T را تقریباً **بله** می‌کنم:

```
Visual QA
Responsive QA
Cross-browser QA
Console QA
HTML validation
Accessibility audit
Lighthouse audit
Broken-link check
Interaction testing
Form validation testing
RTL/LTR QA
Light/Dark QA
Persian/English QA
Regression QA
```

و فایل:

```
QA.md
```

هم خواهیم داشت.

---

# 14. Git Workflow

برای پروژه solo، branch جدا برای هر feature بیش‌ازحد است.

پیشنهاد:

```
main
development
```

و commitهای کوچک:

```
feat:
fix:
refactor:
docs:
style:
perf:
test:
chore:
```

Phase checkpoint هم خواهیم داشت.

Codex **نباید خودش commit کند مگر ما در همان فاز از او بخواهیم**؛ ولی باید commit پیشنهادی بدهد.

---

# 15. معماری رفتار Codex

این قسمت Master Prompt بسیار سخت‌گیرانه خواهد شد.

Codex در هر Phase:

```
1. Inspect
2. Reason
3. Challenge requirements if needed
4. Produce implementation plan
5. Identify affected files
6. Identify risks
7. Wait/continue according to phase instructions
8. Implement only current scope
9. Run relevant checks
10. Fix failures
11. Self-review diff
12. Report results
13. STOP
```

مهم:

> **هرگز خودسر وارد Phase بعدی نشود.**

---

# 16. Hero را اول می‌سازیم

پیشنهاد سؤال W5 من: **بله**.

بعد از Design System:

> Header + Hero را به Production Quality می‌رسانیم.

چرا؟

چون Hero سریع مشخص می‌کند:

- typography درست است یا نه
- spacing درست است یا نه
- illustration style جواب می‌دهد یا نه
- palette جواب می‌دهد یا نه
- dark/light جواب می‌دهد یا نه
- responsive language جواب می‌دهد یا نه

اگر Hero ضعیف باشد، ساختن ۱۰ سکشن بعدی فقط تکثیر یک Design Direction ضعیف است.

---

# 17. قبل از Hero باید Wireframe داشته باشیم

ترتیب:

```
Positioning
↓
Buyer Persona
↓
Content Strategy
↓
Information Architecture
↓
Conversion Flow
↓
Page/Site Map
↓
Text Wireframe
↓
Design System
↓
Hero Prototype
↓
Full Implementation
```

نه:

```
Open Codex
↓
"Create beautiful portfolio"
```

---

# 18. MVP در این پروژه معنی «ناقص» نمی‌دهد

V1 باید polished باشد.

اما لازم نیست ۲۰ قابلیت داشته باشد.

اصل ما:

> **Small feature set, extremely well executed.**

مثلاً Coming Soon را از v1 حذف می‌کنم.

Privacy/Terms را هم برای قالب portfolio ضروری نمی‌دانم.

Login/Register قطعاً حذف.

Pricing هم حذف.

این‌ها noise هستند.

---

# پیشنهاد ساختار فعلی محصول

من فعلاً این ساختار را پیشنهاد می‌کنم:

```
Home
About
Portfolio
Portfolio Details
Services
Blog
Blog Details
Contact
404
```

ولی Home خودش شامل:

```
Hero
Trusted/availability indicator
About preview
Skills / stack
Selected projects
Services
Experience
Testimonials
Blog preview
CTA
Footer
```

خواهد بود.

این ساختار **چندصفحه‌ای ولی focused** است.

---

# یک قابلیت متمایز که پیشنهاد می‌کنم

به‌جای «چند Home تصادفی»، محصول را حول یک سیستم واقعی بسازیم:

## Adaptive Portfolio Presentation System

خریدار بتواند Portfolio را با سه نوع پروژه نمایش دهد:

```
Web Development
UI/UX Design
Freelance / Client Work
```

و project detail صفحه‌ای جدی داشته باشد که شامل:

```
Project overview
Challenge
Role
Stack
Process
Solution
Screenshots
Results
Next project
```

باشد.

یعنی قالب فقط «یک رزومه خوشگل» نباشد؛ واقعاً به کاربر کمک کند **خودش و پروژه‌هایش را بفروشد**.

این تفاوت ارزشمند است.

---

# Buyer Persona پیشنهادی

من Buyer Persona را تقریباً این‌طور می‌بینم:

> **یک برنامه‌نویس، طراح یا فریلنسر ایرانی ۲۰ تا ۳۵ ساله که مهارت فنی دارد، ولی نمی‌خواهد هفته‌ها برای طراحی Portfolio خودش وقت بگذارد. او یک قالب مدرن، فارسی، سریع، قابل شخصی‌سازی و حرفه‌ای می‌خواهد تا پروژه‌ها، مهارت‌ها، تجربه و اطلاعات تماسش را نمایش دهد و برای استخدام یا گرفتن پروژه استفاده کند.**

این با بازار دسته شخصی راست‌چین نیز هم‌راستاست؛ خود راست‌چین برای این دسته بر رزومه، سابقه کاری، نمونه‌کار، شخصی‌سازی، responsive بودن، کدنویسی استاندارد و فرم تماس تأکید می‌کند. [راست چین](https://www.rtl-theme.com/category/template-html/personal-html/)

---

# برنامه Update محصول

برای سؤال A7:

پیشنهاد:

```
v1.0.0 → Initial commercial release

v1.0.1 → Bug fixes after launch

v1.1.0 → improvements based on first buyers

v1.2.0 → new portfolio components / project layouts

v2.0.0 → only if product achieves meaningful traction
```

نه اینکه هر ماه Feature بی‌دلیل اضافه کنیم.

---

# نسخه Pro؟

فعلاً **نه**.

تا وقتی v1 حداقل سیگنال فروش واقعی نداده:

> ساخت Pro = speculative work.

اگر محصول مثلاً ۳۰–۵۰ فروش گرفت و کاربران درخواست مشخصی داشتند، آن وقت:

```
v2
یا
Pro
```

را بررسی می‌کنیم.

---

# قیمت اولیه پیشنهادی

با وضعیت فعلی بازار شخصی که نمونه‌های جدید حدود ۶۲۵–۸۹۵ هزار تومان و بعضی محصولات بالاتر از یک میلیون تومان دیده می‌شوند، من برای محصول اول به جای قیمت‌گذاری خیلی ارزان پیشنهاد می‌کنم محدوده‌ی:

**حدود ۶۵۰ تا ۷۵۰ هزار تومان**

را بررسی کنیم و در صورت امکان با **launch discount** جذاب وارد شویم. محصولات بیش از حد ارزان گاهی به‌جای «ارزش خرید بالا»، پیام «محصول ضعیف‌تر» می‌دهند. [راست چین](https://www.rtl-theme.com/category/template-html/personal-html/)

قیمت نهایی را الان قفل نمی‌کنیم.

---

# Round 2 — این بار فقط سؤال‌های تعیین‌کننده

این‌ها را جواب بده. دیگر ۲۵۰ سؤال نداریم. 😄

### 1. هویت دقیق محصول

کدام را انتخاب می‌کنی؟

**A)** فقط Developer Portfolio  
**B)** Developer + Designer Portfolio  
**C)** Developer + Designer + Freelancer Portfolio  
**D)** General Personal Portfolio برای همه حرفه‌ها

پیشنهاد من: **C**

---

### 2. Demo Persona

Demo اصلی چه کسی باشد؟

مثلاً:

> «آرین — Frontend Developer & UI Engineer»

یا:

> «کیان — Creative Developer & Freelancer»

دوست داری شخصیت Demo **مرد، زن یا کاملاً neutral** باشد؟

---

### 3. آیا مخاطب اصلی هدف استخدام است یا گرفتن پروژه؟

یکی را Primary کنیم:

**A)** استخدام شدن  
**B)** گرفتن پروژه فریلنسری  
**C)** personal branding  
**D)** ترکیب، ولی یکی Primary

پیشنهاد من:

**B + C، با B به‌عنوان primary.**

---

### 4. Multi-home

دو رویکرد:

**A)** فقط یک Home فوق‌العاده polished

یا:

**B)** دو Home با Art Direction متفاوت

مثلاً:

```
Home 01 — Minimal Developer
Home 02 — Creative Freelancer
```

پیشنهاد من برای v1:

**دو Home**، ولی نه بیشتر.

این می‌تواند ارزش خرید را محسوس بالا ببرد.

---

### 5. رنگ اصلی

کدام خانواده بیشتر به سلیقه‌ات نزدیک است؟

**A)** Violet / Indigo  
**B)** Blue / Cyan  
**C)** Emerald / Teal  
**D)** Orange / Coral  
**E)** Monochrome + یک accent خاص  
**F)** هنوز نمی‌دانم؛ بعد از PDF referenceها تصمیم بگیریم

من F را ترجیح می‌دهم.

---

### 6. Hero

کدام direction؟

**A)** تصویر شخص + typography بزرگ  
**B)** abstract illustration  
**C)** code/interface-inspired illustration  
**D)** profile + floating UI cards  
**E)** ترکیبی و خلاقانه

پیشنهاد من:

**D یا E.**

---

### 7. عکس فرد در Hero

آیا Demo باید **عکس واقعی یک فرد** داشته باشد؟

این تصمیم Design را خیلی تغییر می‌دهد.

---

### 8. Portfolio presentation

آیا موافقی project detail یکی از قوی‌ترین قسمت‌های محصول باشد و صرفاً یک modal ساده نباشد؟

پیشنهاد من: **قطعاً بله.**

---

### 9. Blog

Blog را واقعاً می‌خواهی یا فقط چون «صفحه بیشتر = محصول بهتر» به نظر می‌رسد؟

اگر خریدار اصلی Developer/Freelancer است، Blog مفید است، ولی الزامی نیست.

---

### 10. Contact

فرم چون backend نداریم:

**A)** فقط frontend validation  
**B)** آماده اتصال به Formspree/Web3Forms و مشابه‌ها  
**C)** هر دو + documentation

پیشنهاد من: **C**، بدون dependency دائمی به سرویس خارجی.

---

### 11. Persian/English architecture

دو انتخاب داریم:

**A)**

```
/fa/
/en/
```

**B)**

```
index.html
index-en.html
```

و فایل‌های جدا.

من **A** را حرفه‌ای‌تر می‌دانم:

```
fa/index.html
en/index.html
```

موافقی؟

---

### 12. RTL/LTR

آیا English واقعاً LTR باشد و فارسی واقعاً RTL، با Design QA مستقل برای هر دو؟

پیشنهاد من: **بله، صددرصد.**

---

### 13. دو Theme

آیا Theme انتخاب‌شده در `localStorage` ذخیره شود تا با refresh باقی بماند؟

پیشنهاد من: بله.

و بار اول:

```
prefers-color-scheme
```

را رعایت کنیم.

---

### 14. Animation personality

کدام نزدیک‌تر است؟

**A)** تقریباً هیچ animation  
**B)** subtle premium  
**C)** noticeable but elegant  
**D)** creative / experimental

از جواب‌هایت برداشت من: **C**.

---

### 15. Cursor effects

Custom cursor / cursor-follow effect می‌خواهی؟

من برای v1 پیشنهاد **نه** می‌دهم مگر PDFهای reference واقعاً آن را توجیه کنند.

---

### 16. Page transitions

Transition بین صفحات می‌خواهی؟

مثلاً fade کوچک.

من پیشنهاد می‌کنم **بسیار محدود یا هیچ**؛ نباید navigation کند شود.

---

### 17. Portfolio filter

مثل:

```
All
Web Apps
Landing Pages
UI Design
Open Source
```

می‌خواهی؟

پیشنهاد من بله.

---

### 18. Skill section

کدام سبک؟

**A)** progress bar با درصد مثل `JavaScript 85%`  
**B)** technology cards  
**C)** grouped stack  
**D)** ترکیب B+C

من A را رد می‌کنم. `JavaScript 85%` تقریباً اطلاعات بی‌معنی است.

پیشنهاد: **D**

---

### 19. Testimonials

آیا داخل Demo قرار دهیم؟

من پیشنهاد می‌کنم بله، ولی با محتوای **demo مشخص** و نه ادعای دروغین درباره مشتری واقعی.

---

### 20. CV Download

دکمه:

> دانلود رزومه

در Hero/Header داشته باشیم؟

به نظرم برای بازار هدف ما feature بسیار مهمی است.

---

### 21. Availability indicator

مثلاً:

> ● آماده همکاری روی پروژه جدید

این micro-feature برای Freelancer Portfolio ارزشمند است.

می‌خواهی؟

من پیشنهاد بله می‌دهم.

---

### 22. GitHub integration

چون backend/API نداریم، دو راه:

**A)** فقط لینک GitHub  
**B)** static GitHub-style contribution/activity component نمایشی

من A را ترجیح می‌دهم؛ fake integration نسازیم.

---

### 23. Social links

کدام‌ها در Demo باشند؟

پیشنهاد من:

```
GitHub
LinkedIn
Telegram
Email
```

Instagram فقط اگر Design Persona آن را لازم داشته باشد.

---

### 24. Documentation

من README تنها را برای محصول تجاری کم می‌دانم.

پیشنهادم:

```
README.md
+
documentation/index.html
```

README برای developer و HTML Documentation برای مشتری.

موافقی؟

---

### 25. فایل نهایی مشتری

پیشنهاد ساختار من:

```
product-package/
│
├── main-files/
│   ├── fa/
│   ├── en/
│   └── assets/
│
├── source/
│   └── development source
│
├── documentation/
│   └── index.html
│
├── changelog.txt
├── credits.txt
└── readme.txt
```

موافقی؟

---

### 26. نام محصول

فعلاً می‌خواهم اسم را **بعد از دیدن PDFهای Design Reference** انتخاب کنیم.

چون اسم باید با personality بصری محصول جور باشد، نه اینکه اول اسم انتخاب کنیم و بعد Design را زورکی با آن هماهنگ کنیم.

موافقی؟

---

### 27. مهم‌ترین سؤال Round 2

بین این دو فلسفه یکی را انتخاب کن:

**A)**

> «یک قالب Portfolio بسیار زیبا»

**B)**

> «ابزاری برای اینکه یک Developer/Freelancer ایرانی خودش، مهارت‌ها و پروژه‌هایش را حرفه‌ای ارائه کند و شانس گرفتن پروژه/فرصت شغلی را افزایش دهد.»

من فقط در صورتی این پروژه را جدی می‌دانم که انتخابمان **B** باشد.

چون B مشخص می‌کند Hero چه بگوید، Portfolio چگونه طراحی شود، CTA چه باشد، About چه اطلاعاتی بدهد، Contact چگونه عمل کند و حتی Blog چه نقشی داشته باشد.

---

بعد از همین **۲۷ جواب**، دیگر سؤال‌های گسترده ندارم.

مرحله بعدی من این خواهد بود:

**Market Positioning → Product Concept → Feature Matrix → Sitemap → Page/Section Architecture → Design Direction → Technical Architecture → QA Gates → Codex Execution Protocol**

و بعد Master Prompt انگلیسی را به‌صورت یک **Context-Engineered Operating Specification** می‌سازم؛ نه یک پرامپت چند پاراگرافی معمولی.

PDF تصاویر مرجع اینستاگرام را هم وقتی آماده کردی بفرست؛ **قبل از نهایی کردن Visual Direction و Master Prompt بررسی‌اش می‌کنم**.