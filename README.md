# Sahm Medical 🏥 | سهم ميدكال

> **Biomedical Equipment, Warehouse & ERP Desktop System**  
> **نظام إدارة المخازن والأجهزة الطبية والشؤون التجارية والصيانة المتكامل**

**Sahm Medical** is a professional desktop ERP application designed for medical device distributors, biomedical engineering centers, and healthcare warehouses. It operates **100% offline**, safeguarding business data locally with maximum performance.

**سهم ميدكال** هو نظام مكتبي متكامل مصمم خصيصاً لموردي وموزعي الأجهزة الطبية، مراكز الهندسة الطبية، ومستودعات التجهيزات الصحية. يعمل البرنامج **محلياً بالكامل بدون إنترنت (Offline-First)** لضمان أقصى درجات الأمان والسرعة.

---

## 🧩 Core Modules & What It Does | الأقسام وماذا يقدم البرنامج

### 1. 🏥 Medical Inventory & S/N Tracking | الأجهزة الطبية وتتبع السيريالات
- **EN:** Tracks each device individually by factory Serial Number (S/N) and company asset code. Manages warranties, technical conditions (new, used, under maintenance), ownership types, and warehouse shelf locations.
- **AR:** تتبع دقيق لكل جهاز منفصل برقم المصنع التسلسلي (S/N) وكود الأصل للشركة، مع متابعة مواقف الضمان، الحالات الفنية، نوع الملكية (شراكة/خاص)، ومواقع التخزين.

### 2. 🔩 Spare Parts & Consumables | مستودع قطع الغيار والمستهلكات
- **EN:** Manages spare parts (O2 sensors, cables, boards, batteries, filters) linked to compatible medical models, with automated low-stock threshold alerts.
- **AR:** إدارة قطع الغيار والمستهلكات الطبية مع ربطها بالأجهزة المتوافقة، وتنبيهات فورية تلقائية عند بلوغ حد الطلب الأدنى.

### 3. 📋 Inventory Audit & Barcode Scanning | الجرد ومطابقة المخزون
- **EN:** Real-time field audit reconciliation for both devices and spare parts via Barcode/QR scanners. Detects discrepancies and prints signed audit sheets.
- **AR:** محرك فحص ميداني لحظي للأجهزة وقطع الغيار باستخدام ماسح الباركود وQR، مع رصد الفروقات وطباعة محاضر الجرد الرسمية للتوقيعات.

### 4. 💼 Invoicing & Commercial | الفواتير والمعاملات التجارية
- **EN:** Full billing cycle (Sales, Purchases, Quotations, and Returns) with payment methods (Cash, Transfer, Cheque, Installments) and official printable invoices.
- **AR:** دورة فواتير كاملة (بيع، شراء، عروض أسعار، مرتجعات) وتعدد طرق السداد (كاش، تحويل، شيكات، أقساط) وطباعة فواتير معتمدة.

### 5. 🛠️ Maintenance & Handover Protocols | الصيانة الهندسية ومحاضر الاستلام
- **EN:** Maintenance tickets covering repairs, periodic calibrations, and refurbishments. Tracks technician labor and consumed parts, and generates formal handover protocols.
- **AR:** تذاكر صيانة للأعطال، المعايرة الدورية، والتجديد الشامل، مع احتساب قطع الغيار المستهلكة وإصدار محاضر استلام وتسليم رسمية وموثقة.

### 6. 🤝 Clients & Suppliers | إدارة العملاء والموردين
- **EN:** Detailed customer balances and account statements. Tracks supplier agencies, partnership models (fixed margin, commission), credit limits, and payment grace periods.
- **AR:** كشوف حسابات تفصيلية للعملاء (مستشفيات، عيادات، معامل)، وإدارة الوكلاء والموردين، نسب وهوامش الأرباح، فترات السماح، وسقوف الائتمان.

### 7. 💰 Expenses & HR Payroll | المصروفات والرواتب وسجل الدوام
- **EN:** Categorized operational expenses (EXP vouchers). Employee profiles, daily attendance tracking (absent/late/overtime), advances, and monthly payroll runs.
- **AR:** تبويب المصروفات التشغيلية بسندات صرف آلية، وإدارة شؤون الموظفين، سجل الحضور والغياب والإضافي، السلف، ومسيرات الرواتب الشهرية.

### 8. 🔒 Offline Engine & Data Portability | التشغيل المحلي والبيانات
- **EN:** Zero cloud dependency via `Dexie.js` (IndexedDB). Instant single-click database backup/restore and comprehensive **Excel (.xlsx)** import/export across all modules.
- **AR:** خصوصية تامة بدون سحابة إلكترونية، مع إمكانية أخذ نسخة احتياطية واستعادتها بضغطة زر، وتصدير واستيراد كافة البيانات عبر ملفات Excel.

---

## 🛠️ Tech Stack | التقنيات المستخدمة

| Layer | Technology |
| :--- | :--- |
| **Frontend Framework** | [Angular](https://angular.dev/) (Standalone Components, Signals & Reactive State) |
| **Desktop Environment** | [Electron](https://www.electronjs.org/) |
| **Local Database** | [Dexie.js](https://dexie.org/) (High-performance IndexedDB wrapper) |
| **Barcode & QR Engine** | `JsBarcode` & `qrcode` |
| **Data Spreadsheets** | `SheetJS (xlsx)` |
| **Packaging & Distribution**| `electron-builder` (Portable Windows `.exe`) |

---

## ⚡ Quick Start & Running | التشغيل والاستخدام

### Direct Usage | تشغيل مباشر للمستخدم:
Run **`Sahm Medical.exe`** directly on Windows without any installation or prerequisites.  
شغّل ملف **`Sahm Medical.exe`** مباشرة على نظام ويندوز دون الحاجة لأي تثبيت أو برامج إضافية.

### Development Commands | أوامر التطوير:
```bash
# 1. Install dependencies | تثبيت الحزم
npm install

# 2. Run web development server | تشغيل خادم الويب (localhost:4200)
npm start

# 3. Launch Desktop Electron app | تشغيل التطبيق المكتبي
npm run desktop

# 4. Build portable Windows executable | بناء ملف exe المحمول في مجلد release
npm run dist
```

---

## 📄 License & Rights | حقوق الملكية

All rights reserved © **سهم ميدكال | Sahm Medical**.
