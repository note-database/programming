پس Round 4 قفل شد.

حالا می‌ریم سراغ **Round 5 — Detailed UX & Interaction Architecture**؛ این مرحله تعیین می‌کند سایت فقط زیبا نباشد، بلکه رفتارش هم دقیق، قابل پیش‌بینی و حرفه‌ای باشد.

1. **ورود کاربر به Homepage چه تجربه‌ای داشته باشد؟**  
    پیشنهاد من: بدون preloader. صفحه سریع باز شود، Hero بلافاصله قابل خواندن باشد، فقط یک reveal کوتاه و subtle روی عناصر اصلی اجرا شود. هیچ تأخیر مصنوعی برای «نمایشی‌تر شدن» سایت نمی‌خواهم.
    
2. **Navigation در اولین viewport چگونه رفتار کند؟**  
    پیشنهاد من: در بالای Hero سبک و integrated باشد؛ پس از Scroll، compact شود و background/border ظریف بگیرد. نباید ناگهان شکل کاملاً متفاوتی پیدا کند.
    
3. **Navigation Active State چگونه مشخص شود؟**  
    پیشنهاد من: بر اساس Section فعلی، آیتم فعال به‌صورت subtle با accent یا underline مشخص شود. نه background pillهای بزرگ برای هر آیتم.
    
4. **Click روی Nav Item چه کند؟**  
    برای Sectionهای موجود در Home، smooth-scroll به anchor. برای `Portfolio` و `Blog` بهتر است یک الگوی شفاف داشته باشیم: یا nav اصلی به page برود و preview داخل Home CTA جدا داشته باشد، یا برعکس.  
    **پیشنهاد من:** `Portfolio` و `Blog` در Navbar مستقیم به صفحات مستقل بروند؛ داخل Homepage previewها CTA خودشان را داشته باشند. این از رفتار دوگانه و مبهم جلوگیری می‌کند.
    
5. **Logo/Name در Navbar چه کند؟**  
    همیشه لینک به Home/top. ساده و predictable.
    
6. **Mobile Menu چگونه باز شود؟**  
    پیشنهاد من: large overlay / full-screen sheet با typography بزرگ، نه dropdown فشرده. باز و بسته شدن باید کوتاه و روان باشد.
    
7. **Mobile Menu چه stateهایی داشته باشد؟**  
    حداقل:
    
    - closed
    - opening
    - open
    - closing  
        و هنگام open:
    - body scroll lock
    - focus trap
    - Escape to close
    - focus return to trigger  
        اینها باید در prompt فنی آینده صریح نوشته شوند.
8. **Theme Toggle چگونه رفتار کند؟**  
    پیشنهاد من:
    
    - first visit → system preference
    - manual choice → ذخیره در localStorage
    - subsequent visit → manual preference بر system اولویت داشته باشد  
        تغییر theme باید بدون flash آزاردهنده باشد.
9. **Theme Toggle animation داشته باشد؟**  
    بله، ولی بسیار کوتاه. icon transition یا rotation کوچک کافی است. کل صفحه نباید با animation سنگین crossfade شود.
    
10. **Language Switcher چگونه باشد؟**  
    چون runtime translation نداریم، `FA / EN` باید بین دو نسخه واقعی لینک کند. اگر کاربر در `portfolio.html` فارسی است و EN را می‌زند، ترجیحاً به معادل انگلیسی همان صفحه برود، نه همیشه Home.
    
11. **Scroll behavior کلی چگونه باشد؟**  
    Native-first. Smooth scrolling سبک. هیچ smooth-scroll library سنگینی توصیه نمی‌کنم مگر بعداً نیاز واقعی پیدا شود.
    
12. **Reduced Motion چه کند؟**  
    در `prefers-reduced-motion: reduce`:
    
    - scroll behavior عادی
    - reveal animations حذف/کوتاه
    - transform-heavy effects غیرفعال
    - hover animationهای ضروری محدود شوند
13. **Hero CTA Primary چه کند؟**  
    `View My Work` → Portfolio page یا Featured Projects.  
    پیشنهاد من برای Demo اصلی: مستقیم به `portfolio.html`، چون Portfolio قلب محصول است.
    
14. **Secondary CTA چه باشد؟**  
    `Download CV` یا `Contact Me`.  
    Developer Demo: Download CV مناسب‌تر.  
    Designer Demo: Contact / Let's Talk می‌تواند قوی‌تر باشد.
    
15. **Availability Badge clickable باشد؟**  
    پیشنهاد من: نه لزوماً. اگر clickable شد باید به Contact برود؛ اگر فقط status است، نباید cursor pointer بگیرد.
    
16. **Featured Projects interaction چگونه باشد؟**  
    Card یا Project Block باید یک لینک اصلی واضح داشته باشد. بهتر است کل visual area clickable باشد ولی title هم semantic link بماند. Nested clickable elements ممنوع.
    
17. **Hover Project چه تغییراتی بدهد؟**  
    پیشنهادی:
    
    - image scale 1–2%
    - subtle overlay
    - metadata reveal
    - cursor change فقط standard pointer  
        بدون parallax سنگین یا tilt.
18. **Keyboard focus روی Project Card چه باشد؟**  
    همان hierarchy بصری hover باید با focus هم قابل درک باشد. تجربه hover-only ممنوع.
    
19. **Portfolio Filter چه UXی داشته باشد؟**  
    پیشنهاد من:
    
    - filter buttons واضح
    - active filter مشخص
    - count اختیاری
    - transition کوتاه
    - بدون layout jump شدید
20. **وقتی Filter نتیجه ندارد چه شود؟**  
    یک Empty State کوچک و واضح نمایش داده شود، نه فضای خالی مبهم.
    
21. **Filter state در URL ذخیره شود؟**  
    برای v1 پیشنهاد من: **نه**. Query string برای چنین محصولی ارزش کمی دارد و complexity اضافه می‌کند.
    
22. **Filter animation چگونه باشد؟**  
    fade + slight translate یا scale بسیار محدود. ارتفاع container نباید با پرش شدید تغییر کند.
    
23. **Project Details چگونه باز شود؟**  
    همیشه صفحه مستقل؛ Modal را برای case-study اصلی پیشنهاد نمی‌کنم.
    
24. **در Project Detail back navigation داشته باشیم؟**  
    بله: `Back to Projects` در بالا یا نزدیک hero و Previous/Next در انتها.
    
25. **Previous/Next Project چگونه انتخاب شود؟**  
    Static و بر اساس HTML. نیازی به JS dynamic پیچیده نیست.
    
26. **Project Gallery Lightbox داشته باشد؟**  
    اینجا پیشنهاد من **بله، ولی optional و سبک** است. اگر تصویر بزرگ ارزش دیدن دارد، Lightbox تجربه خوبی می‌دهد. اگر اضافه کنیم باید keyboard navigation، ESC و focus management درست باشد. اگر اجرای accessible سخت شد، حذفش بهتر از اجرای نصفه است.
    
27. **Gallery روی Mobile چه رفتاری داشته باشد؟**  
    تصاویر stack شوند؛ horizontal carousel فقط اگر واقعاً دلیل طراحی داشته باشد. Swipe carousel به‌صورت پیش‌فرض پیشنهاد نمی‌کنم.
    
28. **Sticky project metadata چه زمانی فعال باشد؟**  
    فقط desktop و وقتی viewport فضای کافی دارد. Tablet/Mobile باید flow عادی داشته باشند.
    
29. **Blog Preview card چه interactionی داشته باشد؟**  
    تصویر + عنوان + meta. Hover بسیار subtle. کل card می‌تواند linked باشد، ولی ساختار HTML semantic حفظ شود.
    
30. **Blog List pagination داشته باشد؟**  
    برای v1 پیشنهاد من: **Static pagination ساده یا اصلاً بدون pagination**. اگر Demo فقط 6 مقاله دارد، pagination ساختگی نکنیم.
    
31. **Reading Time واقعی باشد یا fake؟**  
    در Demo می‌تواند عدد static باشد، ولی باید با حجم مقاله تقریباً هم‌خوانی داشته باشد. عددهای بی‌معنی اعتماد را کم می‌کنند.
    
32. **Blog Detail Table of Contents داشته باشد؟**  
    پیشنهاد من: **نه در v1**. مگر مقاله نمونه خیلی بلند باشد. Portfolio template نباید تبدیل به blogging platform شود.
    
33. **Share buttons داشته باشیم؟**  
    Optional. بهتر است لینک‌های ساده باشند. integration پیچیده social SDK نمی‌خواهیم.
    
34. **Contact Form validation داشته باشد؟**  
    حتی UI-only، **بله**. HTML native validation + enhancement سبک JS. کاربر باید بداند کدام field مشکل دارد.
    
35. **بعد از Submit چه شود اگر backend نداریم؟**  
    این نکته حیاتی است. نباید fake success message بدهیم. پیشنهاد من در Demo:
    
    - prevent actual misleading submit
    - یک واضح demo-state یا documentation note  
        یا form action placeholder مشخص باشد. در نسخه فروش، باید کاملاً معلوم باشد backend لازم است.
36. **Contact field labels؟**  
    label واقعی بالای input. Placeholder فقط مثال؛ نه جایگزین label.
    
37. **Form errors چگونه نمایش داده شوند؟**  
    inline، نزدیک field، readable و accessible. فقط تغییر border به قرمز کافی نیست.
    
38. **Back-to-top چه زمانی ظاهر شود؟**  
    بعد از حدود 1.5–2 viewport scroll. باید با keyboard هم کار کند و روی mobile مزاحم نباشد.
    
39. **Footer CTA interaction؟**  
    CTA به Contact anchor/page. animation کم. Footer نباید یک Hero دوم شود.
    
40. **External links چگونه باز شوند؟**  
    لینک Live Project یا GitHub می‌تواند `target="_blank"` داشته باشد، همراه با `rel="noopener noreferrer"`. لینک‌های داخلی same-tab.
    
41. **PDF CV لینک چگونه باشد؟**  
    می‌تواند download attribute داشته باشد، ولی cross-browser fallback باید قابل قبول باشد.
    
42. **Broken image fallback؟**  
    پیشنهاد من: Documentation و QA جلویش را بگیرد؛ JS fallback نمایشی اضافه نکنیم مگر نیاز واقعی. Placeholderهای خراب نباید masking شوند.
    
43. **Long content edge case تست شود؟**  
    حتماً:
    
    - نام طولانی
    - project title طولانی
    - tagهای زیاد
    - فارسی چندخطی
    - email بلند  
        UI نباید فقط با محتوای Demo زیبا باشد.
44. **RTL interaction mirroring چقدر جدی باشد؟**  
    Previous/Next arrows، directional chevrons، text alignment و motion باید RTL-aware باشند. اما iconهایی مثل play، download یا external-link mirror نمی‌شوند.
    
45. **Focus order در RTL تغییر کند؟**  
    DOM order باید semantic بماند؛ فقط visual mirroring نباید keyboard order را خراب کند.
    
46. **Skip Link داشته باشیم؟**  
    پیشنهاد من: بله. `Skip to main content` برای keyboard users. visually hidden until focused.
    
47. **404 UX چگونه باشد؟**  
    پیام کوتاه + Home CTA + Portfolio CTA. نه dead-end.
    
48. **Error tolerance در JS چگونه باشد؟**  
    اگر یک element optional حذف شد، script نباید crash کند. هر module قبل از bind کردن باید existence check داشته باشد. این برای customization خریدار بسیار مهم است.
    
49. **JS architecture UX-related چگونه باشد؟**  
    feature-based initializers:  
    `initTheme()`, `initNavigation()`, `initPortfolioFilter()`, `initBackToTop()` و...  
    حذف HTML مربوط به یک Feature نباید بقیه script را بشکند.
    
50. **آیا URL hash برای Home sectionها حفظ شود؟**  
    بله، اگر anchor navigation داریم. این رفتار طبیعی web است و deep-linking ساده را ممکن می‌کند.
    
51. **Sticky Nav هنگام anchor scroll header offset را چطور حل کند؟**  
    با `scroll-margin-top` روی Sectionها، نه hackهای JS پیچیده.
    
52. **Auto-highlight nav با IntersectionObserver؟**  
    پیشنهاد من: بله برای anchorهای Homepage. سبک، استاندارد و تمیز.
    
53. **Active nav هنگام Portfolio/Blog page؟**  
    باید بر اساس page-level state مشخص باشد، نه scroll observer.
    
54. **Mobile portfolio filters چگونه باشند؟**  
    اگر جا کم شد، horizontal scroll chip row بهتر از dropdown پنهان است، مگر تعداد category زیاد باشد.
    
55. **Touch hover dependency؟**  
    هیچ اطلاعات مهمی فقط روی hover ظاهر نشود. Mobile باید metadata را بدون hover ببیند.
    
56. **Image lazy loading؟**  
    بله برای تصاویر below-the-fold. Hero image باید eager/high priority باشد.
    
57. **Skeleton loader؟**  
    پیشنهاد من: نه. برای static HTML portfolio لازم نیست. performance خوب بهتر از loader نمایشی است.
    
58. **Page loading transitions؟**  
    پیشنهاد من: نه در v1. Browser navigation استاندارد. اگر motion transition می‌خواهیم، فقط داخل صفحه.
    
59. **Scroll progress indicator؟**  
    برای Homepage نه. برای Blog Detail شاید جذاب باشد ولی فعلاً پیشنهاد من: **خارج از v1**.
    
60. **UX Principle نهایی من برای کل محصول:**
    
    > Every interaction must either improve navigation, understanding, feedback, or delight — otherwise remove it.
    

### پیشنهاد رسمی من برای Round 5

من تقریباً تمام موارد بالا را به‌عنوان baseline توصیه می‌کنم. فقط سه تصمیم را می‌خواهم خودت explicitly تأیید کنی:

**A)** Navbar Portfolio/Blog مستقیم به صفحات مستقل بروند و previewهای Home CTA جدا داشته باشند.  
**B)** Project Gallery یک Lightbox accessible و سبک داشته باشد، مشروط به اینکه بدون dependency سنگین پیاده شود.  
**C)** Contact Form در v1 هیچ success جعلی نشان ندهد و واضح UI-only باقی بماند.

اگر این سه مورد را هم تأیید کنی، **Round 5 قفل می‌شود** و می‌رویم سراغ **Round 6 — Design System Specification**؛ آنجا دقیقاً درباره tokenها، spacing scale، type scale، radius، border، shadows، color roles، dark/light mapping، icon sizing، container system و naming conventions تصمیم می‌گیریم.