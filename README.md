<div align="center">

# 🚀 OpenKM Document Management System 6.3.13

**An enterprise document-management codebase providing repositories, search, workflows, permissions, audit logs and automation.**

<img alt="Languages" src="https://img.shields.io/badge/docs-English_·_فارسی_·_العربية-2563eb?style=for-the-badge">
<img alt="Architecture" src="https://img.shields.io/badge/architecture-Mermaid-7c3aed?style=for-the-badge">
<img alt="Organization" src="https://img.shields.io/badge/org-Barmana--BRM-0f172a?style=for-the-badge">

[English](#english) · [فارسی](#فارسی) · [العربية](#العربية) · [Build Guide](./BUILD.md)

</div>

> [!IMPORTANT]
> **Verified repository status:** Upstream OpenKM source snapshot; legacy Java stack

## 🧭 Architecture

```mermaid
flowchart LR
  U[Browser/WebDAV/API] --> W[Tomcat + WAR]
W --> G[GWT/Spring]
G --> H[Hibernate/workflow]
H --> DB[(Database)]
G --> IDX[(Lucene)]
G --> FS[(Documents)]
```

---

## English

### 📌 Overview

An enterprise document-management codebase providing repositories, search, workflows, permissions, audit logs and automation.

This README is based on the current public source, dependency manifests, container files and runnable entry points. Implemented functionality is separated from roadmap claims, and known limitations are recorded instead of being hidden behind generic setup instructions.

### ✨ Core capabilities

- Document repository and metadata
- Role-based permissions
- Full-text search
- Workflow and automation

### 🧱 Technology stack

| Layer | Technology |
|---|---|
| Packaging | Maven WAR |
| Runtime | Java 8, Tomcat |
| Web | GWT 2.8.2, Spring 3.2.18 |
| Data/Search | Hibernate 3.6, Lucene |
| Version | OpenKM 6.3.13 |

### 🔄 Operating model

1. Prepare the runtime and external services documented in [BUILD.md](./BUILD.md).
2. Configure secrets in local environment files or a secret manager; never commit them.
3. Start infrastructure and backend services before the user interface in multi-service projects.
4. Validate health checks, migrations, model files and provider connectivity.
5. Run tests and domain-specific validation before producing a release artifact.

### 🔐 Security, quality and limitations

- Legacy dependencies require isolation/security review
- Later OpenKM versions have different licensing

### 🛠 Build and deployment

Use **[BUILD.md](./BUILD.md)** for verified prerequisites, development commands, production build steps, tests and troubleshooting.

### 📄 Attribution and license

This is OpenKM upstream code. Preserve OpenKM copyright, license/EULA, trademarks and contributor attribution.

---

## فارسی

### 📌 معرفی پروژه

کدبیس مدیریت اسناد سازمانی با مخزن، جست‌وجو، گردش کار، مجوز، لاگ و خودکارسازی.

این مستند بر اساس سورس عمومی فعلی، فایل‌های وابستگی، تنظیمات کانتینر و نقاط ورود قابل مشاهده تهیه شده است. قابلیت‌های پیاده‌سازی‌شده از موارد نقشه راه جدا شده‌اند و محدودیت‌های واقعی Build به‌صورت شفاف ثبت شده‌اند.

### ✨ قابلیت‌های اصلی

- مخزن سند و فراداده
- مجوز نقش‌محور
- جست‌وجوی تمام‌متن
- گردش کار و خودکارسازی

### 🧱 پشته فناوری

| Layer | Technology |
|---|---|
| Packaging | Maven WAR |
| Runtime | Java 8, Tomcat |
| Web | GWT 2.8.2, Spring 3.2.18 |
| Data/Search | Hibernate 3.6, Lucene |
| Version | OpenKM 6.3.13 |

### 🔄 روند اجرا

۱. پیش‌نیازها و سرویس‌های بیرونی مندرج در [BUILD.md](./BUILD.md) را آماده کنید.  
۲. کلیدها را فقط در فایل محیطی خارج از Git یا Secret Manager نگه دارید.  
۳. در پروژه چندسرویسی، ابتدا دیتابیس، صف و بک‌اند و سپس رابط کاربری را اجرا کنید.  
۴. Health Check، Migration، فایل مدل و اتصال Providerها را بررسی کنید.  
۵. پیش از انتشار، تست فنی و اعتبارسنجی تخصصی حوزه را انجام دهید.

### 🔐 امنیت و محدودیت

- نسخه Runtime و Dependencyها را با Lockfile تثبیت کنید.
- اطلاعات شخصی، فایل آپلودی، کلید API و داده واقعی نباید وارد مخزن عمومی شود.
- ادعاهای دقت، امنیت یا آمادگی Production باید در محیط هدف دوباره ارزیابی شوند.
- محدودیت‌های اختصاصی پروژه در بخش انگلیسی بالا و `BUILD.md` ثبت شده‌اند.

### 🛠 نصب و Build

راهنمای کامل و دستورات قابل کپی در **[BUILD.md](./BUILD.md)** قرار دارد.

### 📄 مجوز و مالکیت

فایل `LICENSE`، اعتبار توسعه‌دهندگان اصلی و مجوز کتابخانه‌های ثالث باید حفظ شود. در پروژه‌های upstream یا fork، مالکیت به سازمان بارمانا منتقل نمی‌شود.

---

## العربية

### 📌 نظرة عامة

قاعدة نظام إدارة مستندات مؤسسي تشمل المستودع والبحث وسير العمل والصلاحيات والتدقيق.

أُعد هذا التوثيق اعتماداً على المصدر العام الحالي وملفات التبعيات والحاويات ونقاط التشغيل المتاحة. وهو يميز بين الوظائف المنفذة وخارطة الطريق ويذكر قيود البناء الفعلية بوضوح.

### ✨ القدرات الأساسية

- مستودع وبيانات وصفية
- صلاحيات حسب الدور
- بحث نصي كامل
- سير عمل وأتمتة

### 🧱 التقنيات

| Layer | Technology |
|---|---|
| Packaging | Maven WAR |
| Runtime | Java 8, Tomcat |
| Web | GWT 2.8.2, Spring 3.2.18 |
| Data/Search | Hibernate 3.6, Lucene |
| Version | OpenKM 6.3.13 |

### 🔄 مسار التشغيل

١. جهز المتطلبات والخدمات الخارجية الواردة في [BUILD.md](./BUILD.md).  
٢. احتفظ بالأسرار في ملف بيئة غير متتبع أو مدير أسرار.  
٣. شغّل قواعد البيانات والطوابير والخلفية قبل الواجهة في الأنظمة متعددة الخدمات.  
٤. تحقق من الصحة والترحيلات وملفات النماذج واتصال المزوّدين.  
٥. نفذ الاختبارات والتحقق المتخصص قبل إصدار نسخة للنشر.

### 🔐 الأمان والقيود

- ثبّت إصدارات التشغيل والتبعيات بملفات القفل.
- لا تضع بيانات شخصية أو ملفات مرفوعة أو مفاتيح API في مستودع عام.
- أعد التحقق من ادعاءات الدقة والأمان والجاهزية في بيئة الهدف.
- القيود الخاصة بالمشروع موثقة في القسم الإنجليزي و`BUILD.md`.

### 🛠 البناء والنشر

توجد التعليمات الكاملة والأوامر القابلة للنسخ في **[BUILD.md](./BUILD.md)**.

### 📄 النسب والترخيص

يجب الحفاظ على `LICENSE` وحقوق المطورين الأصليين وتراخيص المكونات الخارجية. وجود نسخة أو fork لا ينقل ملكية المصدر إلى Barmana-BRM.



---

<div align="center">

Made documentation-ready for the public portfolio of **Barmana-BRM**

</div>
