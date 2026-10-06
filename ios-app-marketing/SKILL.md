---
name: ios-app-marketing
description: "Use for Halim's iOS mobile app business: reverse-engineering how successful apps market and monetize (200k+ installs, $50k-$500k+ revenue) from X.com posts, indie hacker threads, App Store pages and TikTok/IG; finding app ideas, positioning, ASO, onboarding/paywall design, pricing, UGC/creator content, launch plans, and fixing apps that get installs but no revenue. Trigger whenever the user shares an x.com link/screenshot of an app success story, asks 'why does this app make money', 'how do I market my app', 'analyze this app', 'my apps make nothing', or wants a growth/monetization plan for any iOS app, even if they don't say 'marketing'."
---

# سكيل تسويق وربح تطبيقات iOS

## الهدف
حليم عندو تطبيقات iOS ما كتجيبش الفلوس. الهدف ماشي نشرحو ليه التطبيقات ديال الناس نجحو، الهدف نفهمو **الميكانيزم** (شنو بالضبط اللي كيدير installs، وشنو اللي كيحول installs لفلوس) ونطبقوه على تطبيقات حليم بخطوات عملية. الحماس ديال تغريدة "$500k فـ 3 شهور" ما كيعطي والو بلا تفكيك.

## اللغة
- النقاش مع حليم: بالدارجة المغربية بالحروف العربية.
- نصوص الإعلانات، سكريبتات الفيديو، عناوين App Store، الـ paywall copy: بالإنجليزية (أو لغة السوق المستهدف).
- أسماء المصطلحات التقنية (ASO, LTV, CAC, trial-to-paid...) كتبقى بالإنجليزية.

## الحقيقة اللي خاصنا نبداو بيها
- التغريدات ديال "كيف دخلت $500k" فيها **survivorship bias** ومرات مبالغة ولا إعلان مخبي لكورس. ما كنصدقوش رقم حتى نلقاو دليل ثاني (انظر قسم التحقق).
- أغلب التطبيقات اللي كتنجح ما نجحاتش بالتسويق وحدو: النيش + المشكل + الـ paywall + الـ distribution كلهم خاصهم يكونو خدامين مع بعض. إلا واحد خاوي، الباقي ما كيعوضوش.
- مشكل حليم غالبا واحد من هادو: (أ) ما كيجيبش installs، (ب) كيجيب installs وما كيدفعوش. التشخيص هو الخطوة الأولى، ماشي النصائح العامة.

## طريقة الخدمة

اختار المسار حسب شنو طلب حليم:

### 1) حليم شارك تغريدة/لينك/سكرين ديال تطبيق ناجح → فكك التطبيق
اتبع `references/teardown-framework.md`. الخلاصة:
1. **جمع المعطيات**: التغريدة، الأرقام المصرح بها، اسم التطبيق، صفحة App Store (الاسم، subtitle، screenshots، تقييمات، IAP والأسعار)، حساب المؤسس، الإعلانات/الفيديوهات اللي كيدير.
2. **تحقق من الأرقام** (انظر أسفل).
3. **فكك 6 طبقات**: المشكل والنيش، العرض (positioning)، قناة الـ distribution، الـ ASO، onboarding + paywall، الـ retention والتسعير.
4. **استخرج "السر" الحقيقي**: جملة وحدة: شنو الحاجة اللي لو حيدناها التطبيق كيموت؟
5. **ترجمها لحليم**: شنو يقدر يدير من هاد الشي فتطبيقاتو، فـ 7 أيام، بتكلفة قليلة.

### 2) حليم بغا أفكار من X → سيستيم الصيد
اتبع `references/x-research-method.md` (كيفاش نجمعو ونصنفو التغريدات، استعمال الحسابات اللي خدمات، سجل الأفكار).

### 3) حليم عندو تطبيق ما كيربحش → تشخيص
اتبع `references/diagnosis-playbook.md`. السؤال الأول: فين كيتسد الفانيل؟
- impressions → page views (ASO/الأيقونة/العنوان)
- page views → downloads (screenshots، التقييمات، النيش)
- downloads → trial/subscribe (onboarding + paywall)
- trial → paid (القيمة الأولى، الإشعارات، السعر)
- paid → renewal (retention)
طلب من حليم الأرقام (App Store Connect، RevenueCat إلا كاين)، وإلا ما عندوش، دير تشخيص بالمعاينة وقول بوضوح أنه تخمين.

### 4) حليم بغا يطلق ولا يسوق تطبيق → خطة
اتبع `references/growth-playbooks.md` (ASO، UGC/creators، TikTok/IG organic، X build-in-public، إعلانات مدفوعة، Apple Search Ads، Product Hunt/Reddit).

## التحقق من الأرقام
تغريدة وحدة ماشي دليل. حاول تلقى على الأقل إشارة مستقلة وحدة:
- RevenueCat / Stripe / App Store Connect screenshots مع التاريخ (كتقدر تتزور، ولكن كتعطي أفضل من لا شيء).
- تقديرات Sensor Tower / Appfigures / AppMagic / data.ai / Appstorespy (التقديرات تقريبية، قول ذلك).
- ترتيب التطبيق فالـ Top Grossing، عدد التقييمات (بشكل عام: كل تقييم ≈ 50-100 download).
- هل صاحب التغريدة كيبيع كورس/Template/Newsletter؟ إلا إيه، خفف الثقة.
- التوقيت: واش الأرقام ديال شهر واحد (مع ads) ولا سنة؟
كتب فالنتيجة مستوى الثقة: **عالي / متوسط / ضعيف** وعلاش.

## الوصول لـ X.com
- `WebFetch` على x.com غالبا كيتبلوكا. جرب: لينك الـ thread فـ Claude in Chrome (انظر سكيل chrome-browser)، ولا خلي حليم يلصق النص/السكرين، ولا استعمل WebSearch باش تلقى نفس المحتوى فمواقع أخرى (threadreader، المدونات، podcasts).
- ما كندورش على الحماية ديال المنصة، وما كنخدموش بحسابات مزورة. إلا طلب تسجيل الدخول، حليم هو اللي يدير.
- كل مرة قول من فين جبتي المعلومة وواش شفتيها بعينك ولا من نسخة ثانية.

## الصيغة ديال الجواب
فكك التطبيق فهاد الشكل (قصير، بلا حشو):
1. **ملخص**: التطبيق، الأرقام المصرح بها، مستوى الثقة.
2. **السر الحقيقي** (جملة وحدة).
3. **الطبقات** (جدول: الطبقة | شنو كيدير | الدليل).
4. **شنو نسرقو (بالمعنى الصحيح: نتعلمو منو)**: 3 حوايج مرتبين.
5. **خطة 7 أيام لتطبيق ديال حليم** مع الأرقام اللي نراقبو (KPI) ومتى نوقفو.
6. **مخاطر**: شنو ممكن ما يخدمش عند حليم وعلاش.

## قواعد
- ما كننسخوش التطبيقات ولا الأيقونات ولا الـ copy ولا الأسماء ديال الناس. كنتعلمو الميكانيزم ونبنيو نسخة أحسن ومختلفة.
- ما كنقترحوش دارك باترنز فالـ paywall (إخفاء الإلغاء، تجربة مجانية مضللة، تقييمات مزورة، شراء reviews). Apple كتبانيها، وكتقتل الحساب.
- ما كنوعدوش حليم بأرباح. كنعطيو فرضيات وتجارب صغيرة بميزانية واضحة، ونقيسو.
- فضل التجارب الرخيصة السريعة (screenshots جداد، subtitle جديد، paywall variant، فيديو UGC) على إعادة بناء التطبيق.
- إلا حليم عطا تطبيق للتحليل، شوف **App Store page** ديالو بحال كلاعب جديد: واش فهمتي شنو كيدير فـ 3 ثواني؟
- آخر كل جلسة: قترح سطر لسجل التعلم `references/learning-log.md` (الأحدث فوق) وزيدو غير بموافقة حليم.

## الملفات
- `references/teardown-framework.md`: قالب تفكيك تطبيق بـ 6 طبقات.
- `references/x-research-method.md`: كيفاش نصيدو الأفكار من X ونصنفوها.
- `references/diagnosis-playbook.md`: تشخيص الفانيل ديال تطبيق ما كيربحش.
- `references/growth-playbooks.md`: قنوات الـ distribution والتجارب.
- `references/learning-log.md`: الدروس والتجارب ديال حليم.
