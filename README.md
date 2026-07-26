# Bank-System

🏦 Bank Management System (C++ Console Application)
A feature-rich C++ Console Application designed for managing bank client data and performing core financial operations. The system uses a persistent, file-based database (Clients.txt) to store, update, and manage account records smoothly without relying on external database engines.

🌟 Key Features & Functionalities
The system is split into two primary menu-driven interfaces:

1️⃣ Main Menu (Client Management)
Show Client List: Displays all registered bank accounts in a clean, auto-aligned table.

Add New Client: Registers a new client record with automatic verification to prevent duplicate account numbers.

Find Client: Searches for an account by its unique Account Number and displays a detailed client card.

Update Client Info: Modifies existing personal details or balances following explicit user confirmation.

Delete Client: Removes an account after verifying its identity and obtaining user confirmation.

2️⃣ Transactions Menu (Financial Operations)
Deposit: Credits a specified amount to a target account and updates the storage file instantly.

Withdraw: Debits an amount from an account with built-in balance checks to prevent overdrawing.

Total Balances: Generates a balance-only report across all client accounts alongside the aggregate total of all funds in the bank.

🛠️ System Architecture & Mechanics (How It Works)
File Persistence: All client records are written to a flat text file (Clients.txt), ensuring data retention across program restarts.

Data Parsing & Serialization: Records are formatted as single-line strings using a custom delimiter (#//#). The program parses and reconstructs these lines into structured data in memory.

Safe Deletion Strategy (Soft Delete): When a record is marked for deletion, it is flagged in memory. The system then rewrites the file, skipping flagged records to guarantee file integrity.

Input Validation & Safety: Protects system logic by blocking invalid operations (e.g., duplicate IDs, withdrawing beyond available funds).

💻 Tech Stack & Applied Concepts
Language: C++

Key Programming Concepts:

Data Structures: Custom structures (struct sClient) and dynamic arrays (std::vector).

File Stream Operations: Input/output file handling via std::fstream.

Console UI Formatting: Dynamic alignment using std::setw and <iomanip>.

Procedural Design: Functional decomposition breaking down tasks into modular, reusable functions.



1️⃣ القائمة الرئيسية (إدارة العملاء)
عرض قائمة العملاء: عرض جميع الحسابات في جدول مرتب ومنسق.

إضافة عميل جديد: تسجيل بيانات عميل جديد مع التأكد التلقائي من عدم تكرار رقم الحساب.

البحث عن عميل: إمكانية البحث برقم الحساب وعرض "بطاقة بيانات" العميل.

تحديث بيانات عميل: تعديل المعلومات الشخصية أو الرصيد بعد تأكيد المستخدم.

حذف عميل: حذف حساب مع التأكد من هوية العميل وتأكيد العملية قبل إتمامها.

2️⃣ قائمة المعاملات المالية (Transactions)
الإيداع (Deposit): إضافة مبالغ إلى حساب معين وتحديث الرصيد مباشرة.

السحب (Withdraw): سحب مبالغ من الحساب مع وجود آلية تحقق تمنع سحب مبلغ أكبر من الرصيد المتاح.

إجمالي الأرصدة: عرض قائمة بأرصدة جميع العملاء وحساب مجموع الأموال الموجودة بالبنك.

🛠️ آلية عمل النظام (How it works)
حفظ البيانات (File Persistence): تُحفظ جميع البيانات في ملف نصي خارجي (Clients.txt) لضمان عدم ضياعها عند إغلاق البرنامج.

معالجة النصوص (Data Parsing): يتم فصل وتجميع البيانات داخل الملف باستخدام رمز فاصل خاص (#//#) لضمان قراءة وسرعة معالجة السجلات.

الحذف الآمن (Soft Delete): عند طلب حذف عميل، يتم استبعاد حسابه وإعادة كتابة الملف بدون البيانات المحذوفة لضمان سلامة الملفات.

حماية المدخلات: يحتوي البرنامج على قيود تُحكم عملية إدخال البيانات، مثل منع تكرار الأرقام التعريفية أو السحب بدون رصيد كافٍ.

💻 التقنيات المستخدمة
اللغة: C++

المفاهيم المطبقة:

الهياكل البيانات (Structs) والناقلات Dynamic Arrays (Vectors).

التعامل مع الملفات وحفظ البيانات (std::fstream).

التنسيق النصي للواجهات (std::setw / iomanip).

البرمجة الإجرائية وت تقسيم المهام لدوال مستقلة (Functions).
