# مهارة المقال والعمود والخاطرة
### (Arabic Essay, Column & Khāṭira Skill)

<p align="center">
  <a href="https://github.com/specailm5/arabic-essay-skill/blob/master/LICENSE"><img alt="License" src="https://img.shields.io/github/license/specailm5/arabic-essay-skill?style=flat-square"></a>
  <a href="https://github.com/specailm5/arabic-essay-skill/commits/master"><img alt="Last commit" src="https://img.shields.io/github/last-commit/specailm5/arabic-essay-skill?style=flat-square"></a>
  <a href="https://specailm5.github.io/arabic-essay-skill/"><img alt="Docs" src="https://img.shields.io/badge/docs-live-brightgreen?style=flat-square"></a>
  <img alt="Agent Skills" src="https://img.shields.io/badge/Agent%20Skills-compatible-5B21B6?style=flat-square">
</p>

**Arabic essay skill for AI agents** — finds the controlling idea, builds the title, opening, body and close, controls voice and rhythm, and diagnoses the draft without flattening the writer: `أهمية القراءة في حياة الإنسان` ← `القراءة التي لا تنفع`. Works with Claude Code, Codex, Antigravity and VS Code agent harnesses.

🔗 **الموقع المرجعي (الأنواع والبنية والأسلوب والنماذج): [specailm5.github.io/arabic-essay-skill](https://specailm5.github.io/arabic-essay-skill/)**

> مهارة برمجية ولغوية لنماذج الذكاء الاصطناعي والمحررات الذكية (Codex، Claude Code، Antigravity IDE، VS Code Agent Harness) لكتابة المقال العربي وتحريره وتشخيص عيوبه، استناداً إلى **«فن المقالة»** لمحمد يوسف نجم، و**«فن المقال الصحفي»** لعبد العزيز شرف، و**«وحي القلم»** لمصطفى صادق الرافعي.

---

## 📖 ما هي المهارة؟

المقال العربي يُكتب كثيراً ويُقرأ قليلاً، والسبب غالباً واحد: **لا فكرة**. أكثر ما يُنشر تحت اسم «مقال» هو موضوع مُعاد ترتيبه، بلا موقف، وبلا دليل، وبلا أثر.

تُمكِّنُ هذه المهارةُ الوكيلَ الذكيَّ من:

1. **تحديد النوع** قبل الكتابة: مقالة أدبية، مقال رأي، عمود، افتتاحية، خاطرة، يوميات، مقال نقدي.
2. **استخراج الفكرة** من الموضوع، واختبارها بالخلاف والإضافة والصدق.
3. **بناء العنوان والمقدمة والعرض والخاتمة** على أساس حركة لا أقسام.
4. **ضبط الصوت** ومنع الوقار المصطنع والوعظ والتكلف.
5. **تشخيص المسودة** في سبعة محاور، وإعطاء تقرير قابل للتنفيذ.

**القواعد الأربع:**
> **فكرة واحدة. صوت صادق. بنية تدفع. ولا كلمة بلا وظيفة.**

---

## 🚀 التثبيت

```bash
npx skills add specailm5/arabic-essay-skill -g -y
```

<details>
<summary>تثبيت يدوي، أو لبيئة واحدة فقط</summary>

**لبيئات محددة:**

```bash
npx skills add specailm5/arabic-essay-skill -a claude-code -a codex
```

**Windows (PowerShell):**

```powershell
$src = "skills\arabic-essay-skill"

New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills\arabic-essay-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.claude\skills\arabic-essay-skill\"

New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.agents\skills\arabic-essay-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.agents\skills\arabic-essay-skill\"

New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.gemini\config\skills\arabic-essay-skill"
Copy-Item -Recurse -Force "$src\*" "$env:USERPROFILE\.gemini\config\skills\arabic-essay-skill\"
```

**macOS / Linux:**

```bash
src=skills/arabic-essay-skill

mkdir -p ~/.claude/skills/arabic-essay-skill
cp -r "$src/." ~/.claude/skills/arabic-essay-skill/

mkdir -p ~/.agents/skills/arabic-essay-skill
cp -r "$src/." ~/.agents/skills/arabic-essay-skill/

mkdir -p ~/.gemini/config/skills/arabic-essay-skill
cp -r "$src/." ~/.gemini/config/skills/arabic-essay-skill/
```

**داخل مشروع واحد (VS Code):**

```powershell
New-Item -ItemType Directory -Force -Path ".agents\skills\arabic-essay-skill"
Copy-Item -Recurse -Force "path\to\skills\arabic-essay-skill\*" ".agents\skills\arabic-essay-skill\"
```

**بدون بيئة برمجية:** انسخ محتوى [`skills/arabic-essay-skill/SKILL.md`](skills/arabic-essay-skill/SKILL.md) إلى التعليمات المخصصة أو System Prompt.

</details>

---

## ⚡ كيف تعمل المهارة؟

### سبعة أسئلة قبل الكتابة

<table dir="rtl" align="right">
<thead>
<tr>
<th align="right">السؤال</th>
<th align="right">لماذا؟</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>ما النوع؟</strong></td>
<td>مقالة أدبية / رأي / عمود / افتتاحية / خاطرة / يوميات</td>
</tr>
<tr>
<td><strong>ما الوظيفة؟</strong></td>
<td>إقناع / تفسير / إمتاع / تسجيل موقف</td>
</tr>
<tr>
<td><strong>من القارئ؟</strong></td>
<td>يحدد المصطلح والافتراضات</td>
</tr>
<tr>
<td><strong>ما الوسيلة والطول؟</strong></td>
<td>يحدد الإيقاع وعدد الأفكار</td>
</tr>
<tr>
<td><strong>ما موقفك؟</strong></td>
<td>يمنع الحياد الكاذب</td>
</tr>
<tr>
<td><strong>إنشاء أم تحرير؟</strong></td>
<td>يحدد شكل المخرج</td>
</tr>
<tr>
<td><strong>ما المحظور؟</strong></td>
<td>دين / سياسة / أشخاص / جهة</td>
</tr>
</tbody>
</table>
<br clear="all">

### الأنواع في سطر

<table dir="rtl" align="right">
<thead>
<tr>
<th align="right">النوع</th>
<th align="right">المركز</th>
<th align="right">الطول</th>
</tr>
</thead>
<tbody>
<tr>
<td><strong>مقالة أدبية ذاتية</strong></td>
<td>تجربة الكاتب</td>
<td>٨٠٠–١٥٠٠</td>
</tr>
<tr>
<td><strong>مقالة موضوعية</strong></td>
<td>تحليل وبرهان</td>
<td>١٠٠٠–٢٥٠٠</td>
</tr>
<tr>
<td><strong>مقال رأي</strong></td>
<td>موقف من قضية</td>
<td>٧٠٠–١٢٠٠</td>
</tr>
<tr>
<td><strong>عمود</strong></td>
<td>رأي + صوت</td>
<td>٥٠٠–٩٠٠</td>
</tr>
<tr>
<td><strong>افتتاحية</strong></td>
<td>رأي المؤسسة</td>
<td>٤٠٠–٨٠٠</td>
</tr>
<tr>
<td><strong>خاطرة</strong></td>
<td>لحظة تأمل</td>
<td>١٥٠–٥٠٠</td>
</tr>
<tr>
<td><strong>يوميات</strong></td>
<td>موقف في زمن</td>
<td>متغيّر</td>
</tr>
</tbody>
</table>
<br clear="all">

### مسار العمل

<pre dir="rtl"><code>
① النوع والقارئ والوظيفة
        ↓
② جملة الفكرة في سطر
        ↓
③ اختبار: خلاف / إضافة / صدق
        ↓
④ الخطة: مقدمة، ثلاث نقاط، خاتمة
        ↓
⑤ العنوان بعد الخطة
        ↓
⑥ المسودة بسرعة
        ↓
⑦ احذف ١٠٪
        ↓
⑧ دقّق: نحو + صورة + لغة + حقائق
</code></pre>

### قبل/بعد

<table dir="rtl" align="right">
<thead>
<tr>
<th align="right">قبل</th>
<th align="right">بعد</th>
<th align="right">السبب</th>
</tr>
</thead>
<tbody>
<tr>
<td>«أهمية القراءة في حياة الإنسان»</td>
<td>«القراءة التي لا تنفع»</td>
<td>مفارقة بدل عنوان عام</td>
</tr>
<tr>
<td>«منذ قديم الزمان…»</td>
<td>مشهد في مكتبة</td>
<td>بداية محسوسة</td>
</tr>
<tr>
<td>«يجب على كل فرد أن يحرص»</td>
<td>«لا أطلب منك أن تقرأ أكثر»</td>
<td>حديث بدل وعظ</td>
</tr>
<tr>
<td>«وفي الختام… نور الحياة»</td>
<td>عودة إلى الشاب</td>
<td>خاتمة دائرة</td>
</tr>
</tbody>
</table>
<br clear="all">

---

## 📚 المراجع والاعتماد

* **«فن المقالة»** — محمد يوسف نجم — الطبعة الرابعة، دار الثقافة، بيروت:
  <https://archive.org/details/maryam_201701>
* **«فن المقال الصحفي»** — عبد العزيز شرف — دار قباء، القاهرة، ٢٠٠٠:
  <https://archive.org/details/BBib-Alex-18773>
* **«وحي القلم»** (الجزء الأول) — مصطفى صادق الرافعي:
  <https://archive.org/details/muhamadaboras05_gmail>

> **إقرار بالفضل:** هذه المهارة صياغة تعليمية مستقلة لمبادئ الكتب الثلاثة، مع نقل اقتباسات محدودة بإسنادها إلى صفحاتها. ولا يتضمّن المستودع نسخاً كاملة من الكتب، ولا يُغني عن الرجوع إلى الأصل.

---

## 🤝 المساهمة

نرحب بالمساهمات التي تحسّن المادة أو التحرير أو التوثيق. اقرأ [CONTRIBUTING.md](CONTRIBUTING.md) قبل فتح طلب سحب، والتزم بـ[قواعد السلوك](CODE_OF_CONDUCT.md).

---

## 🛡️ الأمان

إن وجدت مشكلة أمنية، فلا تفتح قضية عامة؛ راجع [SECURITY.md](SECURITY.md).

---

## 📄 سجل التغييرات

راجع [CHANGELOG.md](CHANGELOG.md) لمعرفة ما أُضيف في كل إصدار.

---

## 📬 الدعم

للأسئلة والاقتراحات: [افتح قضية](https://github.com/specailm5/arabic-essay-skill/issues).

---

## 📜 الترخيص (License)

هذه المهارة مفتوحة المصدر تحت رخصة [MIT](LICENSE)، ومتاحة للاستخدام الشخصي والتجاري والبحثي لدعم اللغة العربية.

