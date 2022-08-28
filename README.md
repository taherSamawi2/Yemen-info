<div dir="rtl" align="justify">

<h1>مشروع Yemen-info </h1> 

هنا بعض الملفات لأهم المعلومات المتعلقة باليمن من ناحية برمجية. لدينا معلومات عن محافظات اليمن ومديرياتها باللغتين العربية والإنجليزية. قُدّمت الأسماء العربية للمحافظات والمديريات بعدة أشكال: بالتشكيل وبدونه، وحتى بصيغة موحّدة نمطية (normalized text).
وقُدّمت الأسماء الإنجليزية بأقرب صورة ممكنة للاسم العربي، وبصيغة أخرى موحّدة كذلك.
هذه الصيغة الموحّدة مفيدة جدًا في البحث في تطبيقات الويب والجوال.

## لماذا؟

لدى العديد من الحكومات مراكز بيانات مفتوحة بمحتوى هائل من المعلومات القيّمة للمبرمجين وعلماء البيانات والباحثين. للأسف، أننا لا نملك شيئًا كهذا، فلهذا قررنا بناءه بأنفسنا.
على سبيل المثال، فسؤال يسير كهذا: "ما المحافظات والمديريات اليمنية مع النطق الصحيح لها؟" متعذّر الإجابة لقلة المعلومات المتوفرة.
هذا المستودع البرمجي سيساعد. نعم، مساعدة قليلة لكنها مفيدة.

## المنهجية والملاحظات

- اختيرت عاصمة لكل محافظة عدا محافظات: أمانة العاصمة، وصنعاء، وعدن لعدم وجود عواصم لها بحسب البيانات. لو كان هناك اختلاف بسيط بين اسم عاصمة المحافظة وأحد المديريات، فهذا يعني أن هذه المديريات هي نفسها عاصمة المحافظة. أحيانا يُزاد على عاصمة المحافظة كلمة "مدينة" وهذا لا يؤثر أنها هي عاصمة المحافظة من بين المديريات. مثًلا، عاصمة محافظة عمران: "مدينة عمران"، وأحد مديريات المحافظة: عمران. هما نفس الشيء. فلماذا لم نُضف كلمة "مدينة" إلى المديرية؟ السبب ملتزمون بشدة بالوثائق الرسمية.

- اخترنا أن نضع اسم عاصمة المحافظة مباشرة تحتها لتسهيل الأمر في جلب المعلومات، ولأن بعض المحافظات ليس لديها عاصمة كما أشرنا آنفًا.

- بذلنا ما في وسعنا لتدقيق المعلومات، ولكن لا نملك ضمانة أيًا كانت على دقة المعلومات المُقدّمة. إن كنت تعلم أي خطًأ أنت متأكد منه، سنرحب بشدة بتعديله.

- أتممنا بحثنا في أغسطس من العام 2022. لذلك، لو كانت المعلومات متقادمة أو غير صحيحة فهذا يعود إلى التغييرات في المحافظات والمديريات على أرض الواقع. نأمل أن نُحدّث المستودع بأحدث المعلومات.

- اخترنا التشكيل بنطق العربية الفصحى على حساب نطق بعض اللهجات المحلية.

- تشكيل الأسماء العربي هو المرجع النهائي للنطق. لو تعارض التشكيل العربي مع النسخة الإنجليزية، فالنطق الصحيح هو في التشكيل العربي. وكما في العادة، لو كنت متأكدًا من النطق الصحيح، أخبرنا للتصحيح.

- في النسخة الإنجليزية من المحافظات والمديريات اخترنا أن نضيف _\*\*Al_ كما هو في الاسم العربي عند التعبير عن "أل التعريف"؛ لأننا نعدها معرّفًا ويمكن حذفها في سياقات مختلفة. مثال عليها مديرية "التحرير" تترجم إلى "Al-Tahrir" بدلًا عن "At Tahrir" والتي قد يفضلها البعض. نحن نفضل الصيغة الأولى للترجمة لما قدّمناه. لو كنت تفضّل الصيغة الثانية يمكنك الاطلاع على [هذا الموقع](https://yemenlg.org/governorates).

- قمنا بتوحيد النصوص لكل محافظة ومديرية. في الأسماء العربية استخدمنا خوارزمية مكتبة [Ar-PHP](https://ar-php.org/github/examples/standard.php). وفي الأسماء الإنجليزية جعلنا التغييرات كالتالي: 1- حذف الفاصلة العليا (')، 2- استبدال الشرطة (-) بمسافة. كل هذه التغييرات المتعلقة بتوحيد النصوص أو كما يُقال تنميطها هي من أجل استرجاع نتائج أفضل في البحث باللغة العربية أو الإنجليزية.

## كيفية الاستخدام

ببساطة، نزّل ملف [yemen-info.json](https://github.com/Yemeni-Open-Source/Yemen-info/blob/main/yemen-info.json) واستخدمه كما يحلو لك. هو عبارة عن ملف JSON، لذلك فهو لا يتعلق بلغة برمجية ولا بإطار عمل معيّن فأكثر اللغات البرمجية تدعمه بسهولة.
لدينا عدة صيغ لنفس المعلومات يمكنك استخدامها لو كنت تفضلها في مجلد [other-formats folder](https://github.com/Yemeni-Open-Source/Yemen-info/tree/main) حيث تجد ملفات:
[yemen-info.csv](./other-formats/yemen-info.csv) و [yemen-info.xlsx](./other-formats/ yemen-info.xlsx) (صيغة ميكروسوفت إكسل)، و [yemen-info.xml](./other-formats/yemen-info.xml)
و [yemen-info.yml]([yemen-info.yml]) و [yemen-info.sql](./other-formats/yemen-info.sql).

يمكنك كذلك استخدام [ملف قاموس cspell](https://github.com/Yemeni-Open-Source/Yemen-info/blob/main/.cspell/custom-dictionary-workspace.txt) لتجاهل أسماء المحافظات والمديريات من تخطئتها من إضافات وبرامج التصحيح الإملائي. كان هذا أمرًا عَرَضيًا عن هدفنا الرئيسي في المشروع ولكننا شاكرون لهذه النتيجة!
يمكنك نسخ قائمة الكلمات لقائمة الاستثناءات لأي محرر نصوص لديه ميزة التصحيح الإملائي، حيث يمكنك إضافتها للقاموس الشخصي لكل لا يعدها البرنامج كلمات خاطئة. هذا موجود في برامج ميكروسوفت وورد، ليبرا أوفيس، وحتى إضافة [Arabic - Code Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker-arabic) على المحرر البرمجي VS Code.

> ملاحظة جانبية: ساهمنا نحن في Yemeni Open Source في الإضافة السابقة الذكر ولمزيد من التفاصيل يمكنك المطالعة على [الرابط](https://github.com/Yemeni-Open-Source/impactful-contributions).

## المميزات

✅ تشكيل عربي كامل لكل محافظة ومديرية.

✅ مفاتيح أرقام الهاتف الثابت لكل محافظة.

✅ ملف قاموس cspell لاستثناء جميع محافظات ومديريات اليمن من تخطئة تسميتها في المصححات الإملائية.

✅ معرف فريد لكل محافظة ومديرية.

✅ عواصم جميع المحافظات من المديريات.

✅ توحيد النصوص (text normalization) لكل محافظة ومديرية سواء باللغة العربية أو الإنجليزية (فعال جدًا في البحث).

✅ العديد من الصيغ المختلفة للبيانات مثل: CSV و XLSX (صيغة ميكروسوفت إكسل) و XML و Yaml و SQL.

## قائمة المهام

- [] نشر الإصدار رقم 1.0.0
- [] إضافة الاوسمة المفيدة في ملف Readme مع رابط النسخة العربية والإنجليزية للملف.
- [] نشر كود برمجي لتحويل ملف JSON مباشرة إلى: CSV و XLSX و XML و Yaml و SQL.
- [] إضافة ميزة GitHub Action لأتمتة العملية السابقة بعد أي عملية commit لملف `yemen-info.json`.

# كيفية المساهمة

يمكنك إضافة issue لو وجدت أي خطأ أو كان لديك اقتراح أو يمكنك إضافة pull request.

ملف `yemen-info.json` هو المصدر الأساسي للبيانات. لو غيّرت شيئًا على هذا الملف ستعمل خيرًا جزيلًا لتعديل نفس البيانات على هذه الملفات:

- [yemen-info.csv]('./other-formats/yemen-info.csv')
- [yemen-info.xlsx](./other-formats/yemen-info.xlsx)
- [yemen-info.xml](./other-formats/yemen-info.xml)
- [yemen-info.yml]('./other-formats/yemen-info.yml')
- [yemen-info.sql]('./other-formats/yemen-info.sql')
  وغيرها من الملفات الأخرى إن وجدت. وتحديث ملف [README.md](https://github.com/Yemeni-Open-Source/Yemen-info/edit/main/README.md) و [README.en.md](https://github.com/Yemeni-Open-Source/Yemen-info/edit/main/README.en.md).

وفي المستقبل سنعمل على أتمتة العملية باستخدام كود برمجي وخدمة GitHub Actions، ونرحب بالمساهمات في هذه المساحة التي ستساعدنا كثيرًا.

## لاحقًا في المستقبل (خارج نطاقنا حاليًا)

هذه قائمة من المهمات المستقبلية خارج نطاقنا حاليًا، ولكن لو وجد الوقت والبيانات ربما سنعمل عليها، وربما نعمل عليها في مستودع آخر.

- إضافة نقاط polygon للخرائط.
- إضافة نقاط الطول والعرض (latitude و longitude) لمراكز المحافظات والمديريات.
- إضافة خريطة تفاعلية جميلة ومفيدة مثل الخريطة على [هذا الموقع](https://yemenlg.org/ar/).

## المصادر

بعض المصادر التي ساعدتنا لإنجاز هذا المشروع:

-

- [مدقّق](https://dictionary.alc.ae/modaqiq) استُخدم لإضافة التشكيل الآلي قبل التحقق اليدوي بأنفسنا.

- [Grammarly](https://app.grammarly.com/) كان مساعدًا كبيرًا على تصحيح الأخطاء الإملائية والنحوية في اللغة الإنجليزية في نسخة ملف Readme الإنجليزية.

- [Countries States Cities Database](https://github.com/dr5hn/countries-states-cities-database) ساعدنا بالمعلومات العامة عن اليمن.

- [الحكم المحلي في اليمن](https://yemenlg.org/ar/) ساعدنا في البيانات عن المديريات لكل محافظة، مع الترجمة الإنجليزية لها.
- [Yemen Information Center](https://yemen-nic.info/yemen/gover/) ساعدنا في البيانات إضافة للمصدر السابق.
- [Yemen Embassy- Cairo](http://www.yemenembassy-cairo.com/aboutyemen6.asp) استخدمناه لمعرفة عاصمة كل محافظة.
- [Ar-PHP](https://github.com/khaled-alshamaa/ar-php) استخدمت هذه المكتبة البرمجية لتوحيد النصوص العربية.  شكرا للمهندس [خالد الشمعة](https://github.com/khaled-alshamaa).

# شكر وامتنان

نشكر كل المساهمين. يمكنك معرفة جميغ المساهمين في صفحة [Contributors Page](https://github.com/Yemeni-Open-Source/Yemen-info/graphs/contributors).

ونشكر كذلك الذين شاركوا في أسماء بعض المديريات اليمنية ولكن لم يشاركوا مباشرة في الكود على المستودع، وهم بالترتيب الأبجدي:
- أمجد الهتاري
- صفوان بنيان
- ضياء الجبوبي
- طلال محرم
- عبداللطيف الرداعي
- يعقوب الكهادي

</div>
