<!-- Database Management System -->
**PostgreSQL** (পোস্টগ্রে এসকিউএল) হল একটি **অ্যাডভান্সড, ওপেন-সোর্স রিলেশনাল ডাটাবেস ম্যানেজমেন্ট সিস্টেম (RDBMS)**, যা মূলত **ডেটা সংরক্ষণ, ম্যানেজমেন্ট এবং রিট্রাইভাল** করার জন্য ব্যবহৃত হয়।

---

### 🔍 **PostgreSQL :**

**PostgreSQL** (উচ্চারণ: পোস্ট-গ্রে-এসকিউএল) একটি **মাইক্রোসফট SQL Server** বা **MySQL** এর মত একটি **ডাটাবেস ম্যানেজমেন্ট সিস্টেম**, যা:

* **বড় আকারের ডেটা সংরক্ষণ** করতে পারে
* **জটিল কোয়েরি** (যেমন JOIN, Subquery) চালাতে পারে
* **ট্রানজেকশন সাপোর্ট করে** (যেমন একাধিক কাজ একসাথে সফল হলে তবেই সব হবে)
* **ACID properties** ফলো করে (যা ডেটার নিরাপত্তা নিশ্চিত করে)
* **Object-Relational Features** রয়েছে (মানে শুধু টেবিল না, ডেটা টাইপ, ফাংশন ইত্যাদিও কাস্টমাইজ করা যায়)

---

### ✅ PostgreSQL এর বৈশিষ্ট্যসমূহ:

1. **ওপেন-সোর্স:** সম্পূর্ণ ফ্রি, চাইলে আপনি নিজেও সোর্স কোড পরিবর্তন করতে পারেন।
2. **Cross-platform:** Windows, Mac, Linux – সব জায়গায় চলে।
3. **Security:** authentication, authorization, SSL encryption সাপোর্ট করে।
4. **Extensibility:** আপনি নিজের ফাংশন, ডেটা টাইপ, অপারেটর ইত্যাদি তৈরি করতে পারেন।
5. **JSON Support:** traditional SQL data ছাড়াও NoSQL এর মত JSON ডেটাও সাপোর্ট করে।

---

### 🎯 কোথায় PostgreSQL ব্যবহার হয়?

* বড় কোম্পানি ও ওয়েব অ্যাপ্লিকেশন (যেমন: Instagram, Reddit)
* ডেটা অ্যানালাইসিস ও রিপোর্টিং সফটওয়্যারে
* ERP, CRM এবং অন্যান্য ব্যাকএন্ড সিস্টেমে

---

### 📌 উদাহরণ (SQL Query):

```sql
CREATE TABLE students (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100),
  age INT
);
```

উপরের কোডটি PostgreSQL-এ একটি students নামের টেবিল তৈরি করে।


নিচে একটি টেবিলের মাধ্যমে **MySQL, PostgreSQL, Oracle, MongoDB** এর মধ্যে পার্থক্য দেখানো হলো:

| Feature                 | MySQL                       | PostgreSQL                   | Oracle DB                  | MongoDB                           |
| ----------------------- | --------------------------- | ---------------------------- | -------------------------- | --------------------------------- |
| **Type**                | Relational DBMS             | Object-Relational DBMS       | Relational DBMS            | NoSQL (Document-based)            |
| **Data Storage Format** | Tables (Rows & Columns)     | Tables + Custom Objects      | Tables (Advanced Features) | JSON-like Documents (BSON)        |
| **Schema**              | Fixed Schema                | Flexible (with custom types) | Strict, Complex Schema     | Dynamic Schema                    |
| **Query Language**      | SQL                         | SQL + Advanced Features      | PL/SQL                     | MongoDB Query Language (MQL)      |
| **ACID Compliance**     | Partial (depends on engine) | Fully ACID Compliant         | Fully ACID Compliant       | Not fully (has support for it)    |
| **Performance**         | Fast Read-heavy Workloads   | Great for Complex Queries    | Optimized for High Volume  | High Performance with Scalability |
| **Open Source**         | Yes                         | Yes                          | No (Proprietary, Paid)     | Yes                               |
| **Best For**            | Web Apps, CMS               | Complex Apps, Analytics      | Enterprise-level Systems   | Big Data, Real-time Apps          |
| **Joins Support**       | Yes                         | Yes (with recursion, etc.)   | Yes                        | No (Embedded Docs used instead)   |
| **Horizontal Scaling**  | Limited                     | Limited                      | Limited                    | Excellent                         |
| **Use Case Examples**   | WordPress, Joomla           | Reddit, Instagram            | Banking, ERP               | Netflix, Uber, Facebook           |

---

### 🔍 সংক্ষেপে:

* **MySQL**: সহজ ও দ্রুত পারফরম্যান্স — Web App, CMS-এর জন্য ভালো।
* **PostgreSQL**: কমপ্লেক্স ডেটা হ্যান্ডেল করে — Advanced Query ও Analytics ভালো।
* **Oracle**: বড় কর্পোরেট ও ব্যাংকিং — Security ও Volume হ্যান্ডেল করে।
* **MongoDB**: NoSQL ডেটাবেজ — Flexible ও Real-time App এর জন্য অসাধারণ।

ডাটাবেজে **Key** মানে হলো এমন একটি কলাম বা কলামের সমষ্টি যা একটি টেবিলের রেকর্ডকে ইউনিক (অদ্বিতীয়) করে চিহ্নিত করতে সাহায্য করে।

---

## 🔐 Key কী?

* **Key** হল ডেটাবেজ টেবিলের এমন একটি অংশ যা **প্রতিটি রেকর্ডকে ইউনিকলি শনাক্ত** করে।
* Key গুলোর মাধ্যমে টেবিলের মধ্যে সম্পর্ক তৈরি করা যায়।

---

## 🔑 Key-এর প্রকারভেদ (Types of Keys):

| Key Name          | বাংলা ব্যাখ্যা                                                        | উদাহরণ                         |
| ----------------- | --------------------------------------------------------------------- | ------------------------------ |
| **Super Key**     | এমন একটি বা একাধিক Attribute যা রেকর্ডকে ইউনিক চিহ্নিত করে            | {Roll}, {Roll, Name}           |
| **Candidate Key** | Super Key-এর মধ্যে সবচেয়ে ছোট বা মিনিমাম Attribute সেট                | {Roll}                         |
| **Primary Key**   | Candidate Key-এর মধ্য থেকে নির্বাচিত ইউনিক এবং NULL-নয় এমন Attribute | Roll (Each student has unique) |
| **Alternate Key** | Candidate Key যেটা Primary Key নয়                                     | Email (যদি Roll primary হয়)    |
| **Composite Key** | একাধিক Attribute মিলে একটি ইউনিক কী তৈরি করে                          | {CourseID, StudentID}          |
| **Foreign Key**   | অন্য টেবিলের Primary Key-এর সাথে সংযোগকারী Key                        | StudentID in "Result" table    |

---

### ✅ উদাহরণ সহ ব্যাখ্যা:

ধরো `Student` টেবিল আছে:

| Roll | Name  | Email                                   |
| ---- | ----- | --------------------------------------- |
| 101  | Rahim | [rahim@mail.com](mailto:rahim@mail.com) |
| 102  | Karim | [karim@mail.com](mailto:karim@mail.com) |

* এখানে `Roll` হলো **Primary Key** (কারণ এটা ইউনিক ও NULL নয়)
* `Email` হতে পারে **Alternate Key** (এটাও ইউনিক কিন্তু Primary হিসেবে ব্যবহৃত হয়নি)
* যদি `Roll` ও `CourseID` একসাথে মিলে রেজাল্ট টেবিলে ইউনিক হয়, তবে সেটা **Composite Key** হবে
* রেজাল্ট টেবিল Student টেবিলের Roll ব্যবহার করলে সেটা **Foreign Key** হবে

নিচে প্রতিটি টপিক খুব সহজভাবে এবং বাংলায় ব্যাখ্যা করা হলো, যাতে তুমি সহজে বুঝতে পারো:

---

### 📌 46-1: Data, Information এবং Database

**⏱ সময়: ১০ মিনিট**

* **Data (ডাটা)**: কাঁচা তথ্য, যেমন: "Affnan", "22", "CSE" এগুলো আলাদা করে কোনো অর্থ দেয় না।
* **Information (তথ্য)**: যখন ডাটাগুলো একসাথে যুক্ত হয়ে অর্থবোধক হয়, তখন সেটা হয় ইনফরমেশন। যেমন: "Affnan is 22 years old and studying CSE".
* **Database (ডাটাবেইস)**: তথ্যগুলোকে গুছিয়ে এক জায়গায় রাখার মাধ্যম। যেমন: একটা কলেজের ছাত্রদের নাম, বয়স, ডিপার্টমেন্ট সব একটি টেবিলে রাখা।

---

### 📌 46-2: DBMS কী এবং কেন ব্যবহার করা হয়?

**⏱ সময়: ১৪ মিনিট**

* **DBMS (Database Management System)**: একটি সফটওয়্যার সিস্টেম যা ডাটাবেইস তৈরি, সংরক্ষণ, পরিচালনা ও অ্যাক্সেস করতে সাহায্য করে।
* **কেন দরকার?**

  * ডাটাগুলো সিস্টেমেটিকভাবে সংরক্ষণ করা যায়।
  * দ্রুত সার্চ করা যায়।
  * একাধিক ইউজার একসাথে কাজ করতে পারে।
  * Data security ও integrity বজায় রাখা যায়।

👉 উদাহরণ: MySQL, Oracle, MongoDB

---

### 📌 46-3: Database Model এবং Relational Model

**⏱ সময়: ১১ মিনিট**

* **Database Model**: ডাটা কীভাবে সংরক্ষণ করা হবে তার ধরন।

  * **Hierarchical Model**: গাছের মতো (parent-child)
  * **Network Model**: অনেক parent-child সম্পর্ক
  * **Relational Model**: টেবিলের মাধ্যমে ডাটা সংরক্ষণ (সবচেয়ে জনপ্রিয়)

👉 Relational Model-এ ডাটাগুলো row এবং column-এ থাকে।

---

### 📌 46-4: Table/Relation-এর গঠন

**⏱ সময়: ৬ মিনিট**

একটি রিলেশন বা টেবিলের গঠন:

* **Row (Tuple)**: একেকটি রেকর্ড বা ইনফরমেশন। যেমন: ১জন ছাত্রের নাম, বয়স, রোল ইত্যাদি।
* **Column (Attribute)**: ডাটার ধরন। যেমন: নাম, বয়স, রোল ইত্যাদি।
* **Table name**: টেবিলের নাম। যেমন: Students

---

### 📌 46-5: Key এবং Super Key কী?

**⏱ সময়: ১৩ মিনিট**

* **Key**: একটি ফিল্ড বা একাধিক ফিল্ড যা ডাটার প্রতিটি রেকর্ডকে আলাদা করে চিনতে সাহায্য করে।
* **Super Key**: যেকোনো key যা রেকর্ডকে ইউনিকভাবে চিহ্নিত করে।

👉 উদাহরণ: Student ID একা বা Student ID + Email একসাথে super key হতে পারে।

---

### 📌 46-6: Candidate, Primary, Alternate, Composite Key

**⏱ সময়: ১১ মিনিট**

* **Candidate Key**: টেবিলে একাধিক field থাকতে পারে যেগুলো ইউনিকভাবে রেকর্ড চিহ্নিত করে।
* **Primary Key**: Candidate key এর মধ্যে যেটাকে বেছে নেওয়া হয়।
* **Alternate Key**: বাকি Candidate key গুলো।
* **Composite Key**: একাধিক কলাম একসাথে মিলিয়ে রেকর্ড চিহ্নিত করে।

👉 উদাহরণ: (Roll, CourseCode) = Composite Key

---

### 📌 46-7: Foreign Key

**⏱ সময়: ৪ মিনিট**

* **Foreign Key**: এক টেবিলের ফিল্ড যা অন্য টেবিলের Primary key এর সাথে যুক্ত।
* এর মাধ্যমে টেবিলগুলোর মধ্যে সম্পর্ক তৈরি হয়।

👉 উদাহরণ: Order টেবিলে CustomerID হলো Foreign Key যা Customer টেবিলের Primary Key এর সাথে যুক্ত।

---

### 📌 46-8: ডাটাবেইস ডিজাইনের টেকনিক

**⏱ সময়: ১১ মিনিট**

ডাটাবেইস ডিজাইনের সময় যা করতে হয়:

1. Requirement Analysis: কী দরকার তা বোঝা
2. Entity & Attribute চিন্তা করা
3. Relationship নির্ধারণ করা
4. Key নির্ধারণ
5. ER Diagram বানানো
6. টেবিলে রূপান্তর

---

### 📌 46-9: Top-down Technique

**⏱ সময়: ১৪ মিনিট**

Top-down design মানে বড় থেকে ছোট দিকে ডিজাইন করা:

1. পুরো সিস্টেম বোঝা
2. Entity গুলা বের করা (যেমন: Student, Course)
3. তাদের Attribute খুঁজে বের করা
4. Relationship খুঁজে বের করা
5. Primary & Foreign Key ঠিক করা
6. ER Diagram আঁকা

---

### 📌 46-10: Relationship এবং Relationship Cardinality

**⏱ সময়: ১০ মিনিট**

* **Relationship**: দুটি entity-এর মধ্যে সংযোগ।

  * Student — Enrolls — Course

* **Cardinality**:

  * One-to-One: একজন ছাত্রের একটি আইডি
  * One-to-Many: একজন শিক্ষক অনেক কোর্স পড়ায়
  * Many-to-Many: অনেক ছাত্র অনেক কোর্সে ভর্তি

---

### 📌 46-11: ER Diagram টুল ও প্রথম ER Diagram তৈরি

**⏱ সময়: ১০ মিনিট**

* **ER Diagram Tools**:

  * Draw\.io
  * Lucidchart
  * dbdiagram.io
  * MySQL Workbench

**ER Diagram বানানোর ধাপ**:

1. Entity নির্ধারণ: যেমন Student, Course
2. Attribute বসানো: যেমন Student-এর জন্য ID, Name
3. Relationship সংযোগ করা
4. Primary Key ও Foreign Key দেখানো

---

Great question!
**ACID** is a set of four key properties that ensure **reliable and consistent transactions in a database**. Here's a simple explanation in **Bengali with examples**:

---

## ✅ ACID মানে কী?

**ACID** হলো:

1. **A - Atomicity (অ্যাটমিকতা)**
   ➤ একটি ট্রানজেকশন হয় পুরোপুরি সম্পন্ন হবে, না হয় একদমই হবে না।
   ❌ মাঝপথে থেমে গেলে সব বাতিল।

   **উদাহরণ:** আপনি অনলাইনে টাকা পাঠাচ্ছেন। যদি ইন্টারনেট বন্ধ হয়ে যায়, তাহলে টাকা কাটা যাবে না বা পাঠানো হবে না — দুটোর একটিও হবে না।

---

2. **C - Consistency (সঙ্গতিপূর্ণতা)**
   ➤ প্রতিটি ট্রানজেকশন শেষ হলে ডাটাবেইসকে সঠিক অবস্থায় রাখতে হবে।
   ❌ ভুল ডেটা বা ভাঙা অবস্থা থাকবে না।

   **উদাহরণ:** কোনো ছাত্র ভর্তি হলে তার নাম, আইডি, কোর্স—সব ঠিকমতো যোগ হবে। কিছু বাদ পড়লে, ভর্তি হবে না।

---

3. **I - Isolation (বিচ্ছিন্নতা)**
   ➤ একাধিক ট্রানজেকশন একসাথে চললেও তারা একে অপরকে প্রভাবিত করবে না।
   ❌ অন্য ট্রানজেকশন মাঝপথে এসে ডেটা পরিবর্তন করতে পারবে না।

   **উদাহরণ:** আপনি আর আপনার বন্ধু একসাথে একটি প্রোডাক্ট অর্ডার দিচ্ছেন। এক জনের অর্ডার অন্য জনেরটিকে প্রভাবিত করবে না।

---

4. **D - Durability (স্থায়িত্ব)**
   ➤ ট্রানজেকশন একবার কমপ্লিট হলে সেটি পার্মানেন্ট।
   ❌ সার্ভার বন্ধ হলেও সেটা হারাবে না।

   **উদাহরণ:** আপনি টাকা পাঠিয়েছেন, আর সার্ভার বন্ধ হয়ে গেছে—তবুও টাকা কাটা থাকবে, কারণ সেটা পার্মানেন্টলি সংরক্ষিত।

---

### 🎯 সংক্ষেপে:

| Property    | কী বোঝায়?                    | উপকারিতা                          |
| ----------- | ---------------------------- | --------------------------------- |
| Atomicity   | সব নাহলে কিছুই না            | ভুল লেনদেন ঠেকায়                  |
| Consistency | ডেটা সব সময় সঠিক             | ভাঙা ডেটা আটকায়                   |
| Isolation   | অন্য ট্রানজেকশনের প্রভাব নেই | একাধিক ইউজার একসাথে কাজ করতে পারে |
| Durability  | একবার লেখা, মানে স্থায়ী      | সার্ভার নষ্ট হলেও ডেটা থাকে       |

---

🧠 PostgreSQL এবং MySQL — দুটিই ACID compliant। তবে PostgreSQL একটু বেশি শক্তিশালী এই দিক থেকে।



# 📘 **47-1: Anomalies (অস্বাভাবিকতা)**


**Anomalies** মানে হচ্ছে ডেটাবেজে কিছু **অনাকাঙ্ক্ষিত সমস্যা**, যা ঘটে যখন টেবিলটি খারাপভাবে ডিজাইন করা হয় বা Normalization না করা হয়। এতে ডেটা আপডেট, ইন্সার্ট বা ডিলিট করার সময় সমস্যার মুখে পড়তে হয়।

Anomalies-এর ৩টি প্রধান ধরন আছে:

1. **Insertion Anomaly** – নতুন ডেটা ঢোকাতে সমস্যা হয়
2. **Update Anomaly** – এক জায়গায় পরিবর্তন করলে অন্য জায়গায় ভুল হয়
3. **Deletion Anomaly** – একটা তথ্য ডিলিট করলে অন্য দরকারি তথ্যও হারিয়ে যায়

---



ধরা যাক আমাদের কাছে নিচের মতো একটি টেবিল আছে:

| **Student\_ID** | **Student\_Name** | **Course** |
| --------------- | ----------------- | ---------- |
| 101             | Ayan              | Math       |
| 102             | Bithi             | Physics    |
| 103             | Ayan              | Chemistry  |

---



### ✅ **1. Insertion Anomaly (ইনসারশন সমস্যা)**

ধরো, তুমি Ayan নামের একজন নতুন শিক্ষার্থীর তথ্য রাখতে চাও, কিন্তু সে এখনো কোনো কোর্সে ভর্তি হয়নি।

তাহলে কী হবে?

আমাদের টেবিলে Course কলাম ফাঁকা রাখতে হবে, যা সাধারণত নিয়মের বাইরে (যদি Not Null constraint দেওয়া থাকে)।

**👉 অর্থাৎ, Course না থাকায় আমরা Ayan-এর তথ্য রাখতে পারছি না। এটিই Insertion Anomaly।**

---

### ✅ **2. Update Anomaly (আপডেট সমস্যা)**

ধরো Ayan-এর নাম "Ayaan" হয়ে গেছে। এখন আমাদের টেবিলে তার নাম দুটি রো-তে আছে:

\| 101 | Ayan | Math |
\| 103 | Ayan | Chemistry |

তুমি যদি ১ম রো-তে নাম আপডেট করো আর ২য়টাতে না করো, তাহলে ডেটা inconsistent হয়ে যাবে।

**👉 অর্থাৎ, সব জায়গায় একসাথে আপডেট করতে না পারলে ডেটায় গড়মিল হয়। এটিই Update Anomaly।**

---

### ✅ **3. Deletion Anomaly (ডিলিশন সমস্যা)**

ধরো Bithi শুধু Physics কোর্স নিয়েছে। যদি তুমি Bithi-এর রেকর্ড মুছে ফেলো, তাহলে Physics কোর্স সম্পর্কিত তথ্যও চলে যাবে — যেটা ভবিষ্যতে দরকার হতে পারে।

**👉 অর্থাৎ, একজন শিক্ষার্থী মুছে ফেললে কোর্স সম্পর্কিত তথ্যও মুছে যাচ্ছে — এটিই Deletion Anomaly।**

---

## ✅ সারসংক্ষেপ:

| ধরণ       | মানে                                    | সমস্যা                                  |
| --------- | --------------------------------------- | --------------------------------------- |
| Insertion | নতুন ডেটা ঢোকাতে সমস্যা                 | কোনো ফিল্ড ফাঁকা রাখতে গেলে সমস্যা      |
| Update    | ডেটা আপডেটে সমস্যা                      | সব জায়গায় ঠিকভাবে আপডেট না হলে গড়মিল হয় |
| Deletion  | ডেটা মুছে ফেললে অতিরিক্ত তথ্যও মুছে যায় | দরকারি তথ্য হারায়                       |



## ✅ **47-2: Functional Dependency (কার্যকর নির্ভরতা)**

### 📖 ব্যাখ্যা:

যখন একটি অ্যাট্রিবিউট (Column) অন্য অ্যাট্রিবিউটের উপর নির্ভর করে, তখন সেটাকে Functional Dependency বলে।

### 📌 উদাহরণ:

| Student\_ID | Student\_Name | Dept |
| ----------- | ------------- | ---- |
| 101         | Ayan          | CSE  |
| 102         | Bithi         | EEE  |

### 🔍 বিশ্লেষণ:

* Student\_ID → Student\_Name
  মানে Student\_ID দিলে Student\_Name জানা যায়।
  এই নির্ভরতার নাম Functional Dependency।

---

## ✅ **47-3: Normalization & 1NF**

### 📖 ব্যাখ্যা:

Normalization হল ডেটা টেবিলকে এমনভাবে সাজানো যাতে Redundancy ও Anomalies কমে যায়।

**1NF (First Normal Form)**:

* প্রতিটি কলামে Atomic (একক) মান থাকতে হবে
* Repeating group থাকা যাবে না

### 📌 উদাহরণ (1NF না থাকা):

| Student\_ID | Name | Subjects      |
| ----------- | ---- | ------------- |
| 1           | Ayan | Math, English |

### 🔍 বিশ্লেষণ:

* Subjects কলামে একাধিক ভ্যালু → 1NF লঙ্ঘন করছে।

### 1NF করার পর:

| Student\_ID | Name | Subject |
| ----------- | ---- | ------- |
| 1           | Ayan | Math    |
| 1           | Ayan | English |

---

## ✅ **47-4: 2NF & Partial Dependency**

### 📖 ব্যাখ্যা:

2NF তখন হয় যখন টেবিল 1NF-এ থাকে এবং **কোনো Partial Dependency না থাকে।**

Partial Dependency মানে: কোনো Column পুরো Primary Key-এর উপর নির্ভর না করে তার অংশবিশেষের উপর নির্ভর করে।

### 📌 উদাহরণ:

| Student\_ID | Course\_ID | Course\_Name  |
| ----------- | ---------- | ------------- |
| 101         | CSE101     | C Programming |

Composite Key: (Student\_ID, Course\_ID)

### 🔍 বিশ্লেষণ:

Course\_Name → Course\_ID এর উপর নির্ভরশীল (Partial Dependency)
2NF করার জন্য এটাকে আলাদা করতে হবে।

---

## ✅ **47-5: 3NF & Transitive Dependency**

### 📖 ব্যাখ্যা:

3NF তখন হয় যখন টেবিল 2NF-এ থাকে এবং **Transitive Dependency না থাকে।**

Transitive Dependency: A → B এবং B → C → তাই A → C

### 📌 উদাহরণ:

| Student\_ID | Name | Dept\_ID | Dept\_Name |
| ----------- | ---- | -------- | ---------- |
| 101         | Ayan | 10       | CSE        |

### 🔍 বিশ্লেষণ:

* Student\_ID → Dept\_ID → Dept\_Name
* তাই Student\_ID → Dept\_Name (Transitive Dependency)
* এটি ভেঙে Dept টেবিল আলাদা করতে হবে।

* চলো আমরা এখন **2NF (Second Normal Form)** এবং **3NF (Third Normal Form)** সহজভাবে বাংলায় শিখি — উদাহরণসহ।

---

## ✅ **2NF (Second Normal Form)**

### 📖 ব্যাখ্যা:

একটা টেবিল **2NF** এ থাকতে হলে:

1. টেবিলটি 1NF এ থাকতে হবে।
2. **Partial Dependency** থাকা যাবে না।

🔹 **Partial Dependency**: যদি কোনো কলাম **composite primary key**-এর *অংশবিশেষের* উপর নির্ভর করে, তাহলে সেটা partial dependency।

---

### 📌 উদাহরণ (2NF না হওয়া):

| Student\_ID | Course\_ID | Student\_Name | Course\_Name  |
| ----------- | ---------- | ------------- | ------------- |
| 101         | CSE101     | Ayan          | C Programming |
| 102         | CSE102     | Bithi         | Java          |

**Composite Primary Key:** (Student\_ID, Course\_ID)

* `Student_Name` → শুধুই `Student_ID` এর উপর নির্ভরশীল ✅
* `Course_Name` → শুধুই `Course_ID` এর উপর নির্ভরশীল ✅
  → তাই এগুলো **partial dependency** হয়ে যাচ্ছে ❌
  (পুরো কম্পোজিট কি’র উপর নির্ভর করছে না)

---

### ✅ সমাধান (2NF তে রূপান্তর):

1. **Student Table:**

| Student\_ID | Student\_Name |
| ----------- | ------------- |
| 101         | Ayan          |
| 102         | Bithi         |

2. **Course Table:**

| Course\_ID | Course\_Name  |
| ---------- | ------------- |
| CSE101     | C Programming |
| CSE102     | Java          |

3. **Enrollment Table (junction):**

| Student\_ID | Course\_ID |
| ----------- | ---------- |
| 101         | CSE101     |
| 102         | CSE102     |

🔍 এখন সব ডিপেন্ডেন্সি আছে নির্ভুলভাবে:

* `Student_Name` → শুধুই `Student_ID`-তে
* `Course_Name` → শুধুই `Course_ID`-তে
* মূল টেবিল (Enrollment) শুধু রিলেশন ধারণ করছে

---

## ✅ **3NF (Third Normal Form)**

### 📖 ব্যাখ্যা:

একটা টেবিল **3NF** এ থাকতে হলে:

1. টেবিলটি 2NF এ থাকতে হবে।
2. কোনো **Transitive Dependency** থাকা যাবে না।

🔹 **Transitive Dependency**: A → B এবং B → C → তাহলে A → C
এবং C কলামটি **Primary key-এ নির্ভরশীল নয় সরাসরি**।

---

### 📌 উদাহরণ (3NF না হওয়া):

| Student\_ID | Student\_Name | Dept\_ID | Dept\_Name |
| ----------- | ------------- | -------- | ---------- |
| 101         | Ayan          | D01      | CSE        |
| 102         | Bithi         | D02      | EEE        |

* `Student_ID` → `Dept_ID`
* `Dept_ID` → `Dept_Name`
* → তাই `Student_ID` → `Dept_Name` (Transitive Dependency ❌)

---

### ✅ সমাধান (3NF তে রূপান্তর):

1. **Student Table:**

| Student\_ID | Student\_Name | Dept\_ID |
| ----------- | ------------- | -------- |
| 101         | Ayan          | D01      |
| 102         | Bithi         | D02      |

2. **Department Table:**

| Dept\_ID | Dept\_Name |
| -------- | ---------- |
| D01      | CSE        |
| D02      | EEE        |

🔍 এখন:

* `Dept_Name` → `Dept_ID` তে নির্ভরশীল (✅)
* `Student_ID` → `Dept_Name` আর নয় (❌ হয়নি)

---

## ✨ সংক্ষেপে মনে রাখো:

| Normal Form | সমস্যা সমাধান করে     | কেমন Dependency বাদ দেয়        |
| ----------- | --------------------- | ------------------------------ |
| 1NF         | Repeating values      | Non-atomic values ❌            |
| 2NF         | Partial dependency    | Composite key-এর অংশে নির্ভর ❌ |
| 3NF         | Transitive dependency | Indirect dependency ❌          |

---




---

**Junction Table দিয়ে Many-to-Many Relationship সমাধান** 

---

## 🔗 **Many-to-Many Relationship** কী?

### 📖 ব্যাখ্যা:

যখন একটি রেকর্ড একাধিক রেকর্ডের সঙ্গে যুক্ত হতে পারে এবং অপর পাশের একটি রেকর্ডও একাধিক রেকর্ডের সঙ্গে যুক্ত হতে পারে — তখন একে **Many-to-Many Relationship** বলা হয়।

> উদাহরণ:
> একজন **ছাত্র** একাধিক **কোর্সে** ভর্তি হতে পারে
> একটি **কোর্স**-এ একাধিক **ছাত্র** থাকতে পারে

---

## ❌ সমস্যাঃ

এই ধরনের Many-to-Many রিলেশন ডিরেক্টভাবে কোনো ডেটাবেজ টেবিলে ম্যানেজ করা যায় না। তাই **Junction Table** ব্যবহার করতে হয়।

---

## ✅ সমাধানঃ Junction Table

Junction Table হলো একটি **মাঝখানের টেবিল** যা দুইটি টেবিলের প্রাইমারি কি নিয়ে একটি নতুন টেবিল তৈরি করে, এবং সেগুলো **Foreign Key** হিসেবে কাজ করে।

---

## 🎓 উদাহরণঃ Student এবং Course

### Step 1: মূল টেবিল দুটি 👇

#### 🧑 Student Table

| student\_id | student\_name |
| ----------- | ------------- |
| 1           | Ayan          |
| 2           | Bithi         |

#### 📚 Course Table

| course\_id | course\_name  |
| ---------- | ------------- |
| 101        | C Programming |
| 102        | Java          |

---

### Step 2: Junction Table বানাই ➡️ **Enrollment Table**

| student\_id | course\_id |
| ----------- | ---------- |
| 1           | 101        |
| 1           | 102        |
| 2           | 101        |

---

## 🔍 বিশ্লেষণ:

* Ayan (`student_id = 1`) → C Programming & Java নিচ্ছে
* Bithi (`student_id = 2`) → C Programming নিচ্ছে

এই Junction Table-এর মাধ্যমে আমরা দেখতে পাচ্ছি কে কোন কোর্স নিচ্ছে।

---

## ✅ কাজের নিয়ম:

* **Primary Key**: Enrollment টেবিলে (student\_id, course\_id) একসাথে **Composite Primary Key** হবে।
* **Foreign Key**:

  * `student_id` → Student Table এর `student_id`
  * `course_id` → Course Table এর `course_id`

---

## 🧠 মনে রাখার কৌশল:

| অংশ       | ব্যাখ্যা                                            |
| --------- | --------------------------------------------------- |
| মূল টেবিল | Student, Course                                     |
| সমস্যা    | একজন ছাত্র অনেক কোর্স নিতে পারে, কোর্সেও অনেক ছাত্র |
| সমাধান    | Junction Table (Enrollment)                         |
| উপকারিতা  | Efficient Query & Relationship Model                |





## ✅ **47-7: Completing the ER Diagram**

### 📖 ব্যাখ্যা:

ER Diagram-এ Entity, Attribute, ও Relationship দেখানো হয়।

* Entity = Box
* Attribute = Oval
* Relationship = Diamond

### 📌 উদাহরণ:

**Student** → takes → **Course**

---

## ✅ **47-8: What is PostgreSQL & Installing**

### 📖 ব্যাখ্যা:

PostgreSQL (Postgres) একটি ওপেন সোর্স RDBMS (Relational DBMS)।
এটি ACID-compliant এবং খুব শক্তিশালী। JSON, Full-text search সাপোর্ট করে।

### 🔍 Installation:

* Download from [https://www.postgresql.org/download/](https://www.postgresql.org/download/)
* pgAdmin GUI দিয়ে চালাতে পারো

---

## ✅ **47-9: Data Flow & PSQL**

### 📖 ব্যাখ্যা:

* Application → Backend → Database → Backend → Application
* **PSQL**: PostgreSQL-এর কমান্ড লাইন টুল

### 📌 উদাহরণ:

```sql
CREATE TABLE students (
  id SERIAL PRIMARY KEY,
  name VARCHAR(50)
);
```



---

## ✅ 1. ডাটাবেজ তৈরি (Create Database)

```sql
CREATE DATABASE mydb;
```

### ডাটাবেজে ঢুকতে (terminal এ):

```bash
\c mydb
```

---

## ✅ 2. টেবিল তৈরি (Create Table)

```sql
CREATE TABLE students (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  age INT,
  email VARCHAR(255) UNIQUE,
  dob DATE,
  contact_no VARCHAR(20),
  developer BOOLEAN
);
```

**SERIAL**: অটো-ইনক্রিমেন্ট হয়।
**VARCHAR**: টেক্সট ফিল্ড
**BOOLEAN**: TRUE/FALSE

---

## ✅ 3. ডেটা যুক্ত করা (Insert Data)

```sql
INSERT INTO students (name, age, email, dob, contact_no, developer)
VALUES
('Affnan Sawad', 20, 'affnan@email.com', '2004-08-19', '01540796323', TRUE);
```

---

## ✅ 4. ডেটা দেখা (Select Data)

```sql
SELECT * FROM students;
```

---

## ✅ 5. ডেটা আপডেট করা (Update Data)

```sql
UPDATE students
SET age = 21
WHERE name = 'Affnan Sawad';
```

---

## ✅ 6. ডেটা ডিলিট করা (Delete Data)

```sql
DELETE FROM students
WHERE name = 'Affnan Sawad';
```

---

## ✅ 7. কিছু কন্ডিশন দিয়ে খোঁজা (Querying with WHERE)

```sql
SELECT * FROM students WHERE age > 20;
SELECT * FROM students WHERE developer = TRUE;
```

---

## ✅ 8. ডেটা sort করা (ORDER BY)

```sql
SELECT * FROM students ORDER BY age DESC;
```

---

## ✅ 9. কিছু ডেটা count করা (Aggregate)

```sql
SELECT COUNT(*) FROM students;
SELECT AVG(age) FROM students;
```




**EXAMPLE**

-- 📌 Create the Students table
CREATE TABLE Students (
  ID SERIAL PRIMARY KEY,
  NAME VARCHAR(255) NOT NULL,
  Age INT,
  Email VARCHAR(255) UNIQUE,
  DOB DATE,
  Contact_No VARCHAR(255),
  DEVELOPER BOOLEAN
);

-- ✅ Insert sample data into Students table
INSERT INTO Students (NAME, Age, Email, DOB, Contact_No, Developer) 
VALUES 
  ('Affnan Sawad', 20, 'affnansawad2002@gmail.com', '2004-08-19', '01540796323', TRUE);

INSERT INTO Students (NAME, Age, Email, DOB, Contact_No, Developer) 
VALUES 
  ('Nusrat Jahan', 22, 'nusrat.jahan99@example.com', '2002-03-15', '01733445566', FALSE),
  ('Mehedi Hasan', 23, 'mehedi.hasan88@example.com', '2001-07-09', '01888776655', TRUE),
  ('Sadia Khatun', 21, 'sadia.khatun22@example.com', '2003-01-25', '01612345678', FALSE),
  ('Rakibul Islam', 24, 'rakibul.islam31@example.com', '2000-11-11', '01911224433', TRUE);

-- 📄 View all students

SELECT * FROM Students;

-- 🔄 Update student's age

UPDATE Students 
SET Age = 21 
WHERE NAME = 'Affnan Sawad';


-- ❌ Delete a student record

DELETE FROM Students 
WHERE NAME = 'Rakibul Islam';

-- 1️⃣ Get students older than 22

SELECT * FROM Students 
WHERE Age > 22;

-- 2️⃣ Get Affnan Sawad with age 21

SELECT * FROM Students 
WHERE Age = 21 AND NAME = 'Affnan Sawad';

-- 3️⃣ Get students older than 20 OR named Affnan Sawad

SELECT * FROM Students 
WHERE Age > 20 OR NAME = 'Affnan Sawad';

--methods

SELECT COUNT(*) FROM students;

SELECT AVG(age) FROM students;


![image](https://github.com/user-attachments/assets/c77c1269-4169-498c-abc6-ac5249a7902e)






---

## ✅ **1. ALTER TABLE: টেবিল Modify করা**

### ➤ নতুন কলাম যোগ:

```sql
ALTER TABLE students ADD COLUMN gender VARCHAR(10);
```

> `students` টেবিলে `gender` নামের নতুন কলাম যোগ হয়েছে।

### ➤ কলামের ডেটাটাইপ পরিবর্তন:

```sql
ALTER TABLE students ALTER COLUMN age TYPE FLOAT;
```

> `age` এর type এখন `FLOAT` হয়ে যাবে।

### ➤ কলাম ডিলিট:

```sql
ALTER TABLE students DROP COLUMN gender;
```

---

## ✅ **2. PRIMARY KEY, UNIQUE কীভাবে ALTER এ সেট করবো**

### ➤ Primary Key সেট:

```sql
ALTER TABLE students ADD PRIMARY KEY (id);
```

### ➤ Unique Constraint:

```sql
ALTER TABLE students ADD CONSTRAINT unique_email UNIQUE (email);
```

---

## ✅ **3. SELECT Queries – Column Alias ও ORDER BY**

### ➤ Column Alias:

```sql
SELECT name AS student_name, age FROM students;
```

> `name` কলামটিকে `student_name` নামে দেখাবে।

### ➤ ORDER BY:

```sql
SELECT * FROM students ORDER BY age DESC;
```

> Age অনুযায়ী বড় থেকে ছোটভাবে সাজাবে।

---

## ✅ **4. WHERE, Logical Operators (AND, OR), Comparison Operators**

### ➤ WHERE:

```sql
SELECT * FROM students WHERE age > 20;
```

### ➤ AND / OR:

```sql
SELECT * FROM students WHERE age > 20 AND developer = TRUE;
SELECT * FROM students WHERE age > 20 OR developer = TRUE;
```

---

## ✅ **5. Scalar & Aggregate Functions**

### ➤ Scalar Function (একটি Row-এর উপর কাজ করে):

```sql
SELECT UPPER(name), LENGTH(name) FROM students;
```

### ➤ Aggregate Functions (পুরো টেবিলের উপর কাজ):

```sql
SELECT COUNT(*), AVG(age), MAX(age), MIN(age) FROM students;
```

---

## ✅ **6. NOT, NULL, COALESCE (Null-Coalescing Operator)**

### ➤ NOT:

```sql
SELECT * FROM students WHERE NOT developer;
```

### ➤ NULL চেক:

```sql
SELECT * FROM students WHERE email IS NULL;
SELECT * FROM students WHERE email IS NOT NULL;
```

### ➤ COALESCE:

```sql
SELECT name, COALESCE(email, 'No Email') FROM students;
```

> `email` যদি NULL হয়, তাহলে 'No Email' দেখাবে।

---

## ✅ **7. IN, BETWEEN, LIKE, ILIKE**

### ➤ IN:

```sql
SELECT * FROM students WHERE age IN (20, 22, 25);
```

### ➤ BETWEEN:

```sql
SELECT * FROM students WHERE age BETWEEN 20 AND 23;
```

### ➤ LIKE (case-sensitive):

```sql
SELECT * FROM students WHERE name LIKE 'A%';  -- A দিয়ে শুরু
```

### ➤ ILIKE (case-insensitive):

```sql
SELECT * FROM students WHERE name ILIKE 'a%';
```

---

## ✅ **8. Pagination: LIMIT ও OFFSET**

### ➤ প্রথম ৫টা রেকর্ড:

```sql
SELECT * FROM students LIMIT 5;
```

### ➤ ৬-১০ নম্বর রেকর্ড:

```sql
SELECT * FROM students LIMIT 5 OFFSET 5;
```

---

## ✅ **9. UPDATE**

### ➤ সাধারণ Update:

```sql
UPDATE students SET age = 21 WHERE name = 'Affnan Sawad';
```

### ➤ একসাথে একাধিক Update:

```sql
UPDATE students SET age = 22, developer = FALSE WHERE id = 3;
```

---

## ✅ **10. DELETE**

```sql
DELETE FROM students WHERE age < 20;
```

---

# PostgreSQL Intermediate Topics 

---

## ✅ **50-1: Date and Date Functions in PostgreSQL**

### ✔ Description:

PostgreSQL-এ DATE ফাংশন ব্যবহার করে তারিখ-সংক্রান্ত কাজ করা যায়। কিছু গুরুত্বপূর্ণ Date ফাংশন:

* `CURRENT_DATE` : বর্তমান তারিখ
* `NOW()` : বর্তমান তারিখ এবং সময়
* `AGE(date)` : নির্দিষ্ট তারিখ থেকে বর্তমান তারিখ পর্যন্ত সময় বের করা
* `EXTRACT(field FROM date)` : বছর, মাস, দিন আলাদা করা যায়

### ✔ Example:

```sql
SELECT CURRENT_DATE;
SELECT NOW();
SELECT AGE('2000-05-15');
SELECT EXTRACT(YEAR FROM DATE '2000-05-15') AS birth_year;
```

### ✔ Explanation:

* `CURRENT_DATE` এখনকার তারিখ
* `NOW()` এখনকার তারিখ ও সময়
* `AGE()` দেয় জন্মদিন থেকে কত বছর, মাস ও দিন হয়েছে
* `EXTRACT()` দিয়ে সাল, মাস, দিন আলাদা করা যায়

---

## ✅ **50-2: GROUP BY and HAVING**

### ✔ Description:

* `GROUP BY`: একই ধরনের ডেটা একত্র করে
* `HAVING`: গ্রুপ করা ডেটা-র ওপর শর্ত দেয়

### ✔ Example:

```sql
SELECT developer, COUNT(*)
FROM students
GROUP BY developer;

SELECT developer, COUNT(*)
FROM students
GROUP BY developer
HAVING COUNT(*) > 1;
```

### ✔ Explanation:

* Developer true/false হিসেবে গ্রুপিং করা হয়েছে
* `HAVING` দিয়ে শুধু সেই গ্রুপ দেখায় যেগুলোর count 1 এর বেশি

দ্বিতীয় টপিক:

### **`GROUP BY` এবং `HAVING` ক্লজ দিয়ে ডেটা গ্রুপিং এবং ফিল্টারিং (50-2)**

---

## 🔶 বিষয়টি কী?

* `GROUP BY`: এটি একই ধরনের ডেটা (একই মান) একসাথে গ্রুপ করে। মূলত Aggregate Function (যেমন: `SUM`, `COUNT`, `AVG`) এর সাথে ব্যবহার হয়।
* `HAVING`: `WHERE` এর মতোই কাজ করে, তবে এটি গ্রুপ করা ডেটার উপর শর্ত দেয়।
  `WHERE` ব্যবহার হয় গ্রুপ করার **আগে**, আর `HAVING` ব্যবহার হয় গ্রুপ করার **পরে**।

---

## ✅ উদাহরণ টেবিল: `students`

| id | name   | department | age | marks |
| -- | ------ | ---------- | --- | ----- |
| 1  | Affnan | CSE        | 20  | 85    |
| 2  | Rakib  | CSE        | 21  | 75    |
| 3  | Nusrat | EEE        | 22  | 90    |
| 4  | Sadia  | CSE        | 21  | 80    |
| 5  | Tanim  | EEE        | 22  | 95    |

---

## 🧠 উদাহরণ ১: প্রতি ডিপার্টমেন্টে কয়জন শিক্ষার্থী আছেন?

```sql
SELECT department, COUNT(*) AS total_students
FROM students
GROUP BY department;
```

### 🔍 ব্যাখ্যা:

* `GROUP BY department`: একই department-এর স্টুডেন্টদের একসাথে করে।
* `COUNT(*)`: প্রতিটি গ্রুপে কয়জন আছেন, তা গণনা করে।

**আউটপুট হবে:**

| department | total\_students |
| ---------- | --------------- |
| CSE        | 3               |
| EEE        | 2               |

---

## 🧠 উদাহরণ ২: যেসব ডিপার্টমেন্টে গড় নম্বর (average marks) 85 এর বেশি

```sql
SELECT department, AVG(marks) AS avg_marks
FROM students
GROUP BY department
HAVING AVG(marks) > 85;
```

### 🔍 ব্যাখ্যা:

* `GROUP BY department`: ডিপার্টমেন্ট অনুযায়ী গ্রুপ করে।
* `AVG(marks)`: গড় নম্বর বের করে।
* `HAVING AVG(marks) > 85`: যেসব গ্রুপের গড় 85 এর বেশি, শুধু তাদেরই দেখায়।

**আউটপুট:**

| department | avg\_marks |
| ---------- | ---------- |
| EEE        | 92.5       |

---

## 📝 সংক্ষেপে:

| বিষয়       | কাজ করে                             |
| ---------- | ----------------------------------- |
| `GROUP BY` | কলামের মান অনুযায়ী রেকর্ড গ্রুপ করে |
| `HAVING`   | গ্রুপ করা ডেটা ফিল্টার করে          |
| `WHERE`    | গ্রুপ করার আগেই রো ফিল্টার করে      |



---

## ✅ **50-3: Foreign Key Constraint**

### ✔ Description:

Foreign Key ব্যবহার করে এক টেবিলের রেকর্ডকে অন্য টেবিলের সাথে সংযুক্ত করা যায়। এটি ডেটার ইনটিগ্রিটি বজায় রাখে।

### ✔ Example:

```sql
CREATE TABLE departments (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100)
);

CREATE TABLE employees (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100),
  dept_id INT REFERENCES departments(id)
);
```

### ✔ Explanation:

`employees` টেবিলের `dept_id` কলামটি `departments` টেবিলের `id` এর foreign key.

---

## ✅ **50-4: Referential Integrity - Insert Behavior**

### ✔ Description:

Foreign key constraint থাকলে, এমন data insert করা যাবে না যা parent টেবিলে নেই।

### ✔ Example:

```sql
INSERT INTO employees (name, dept_id)
VALUES ('Rahim', 1); -- যদি departments table-এ id = 1 না থাকে, insert হবে না
```


অবশ্যই! নিচে PostgreSQL-এর **টপিক ৩ এবং ৪** (Foreign Key এবং Referential Integrity during insert) সহজভাবে বাংলায় ব্যাখ্যা করা হলো উদাহরণসহ:

---



### 🔶 সংজ্ঞা:

Referential Integrity মানে হলো – টেবিলের মধ্যে সম্পর্ক ঠিকভাবে রক্ষা করা।
যেমন: আপনি `students` টেবিলে এমন `dept_id` দিতে পারবেন না যেটা `departments` টেবিলে নেই। এটা নিশ্চিত করে Foreign Key।

---

### 🎯 মূল বিষয়:

* আপনি **child table**-এ এমন Foreign Key ঢুকাতে পারবেন না, যেটা **parent table**-এ নাই।
* Parent টেবিলে আগে ডেটা থাকতে হবে।
* এটি ডেটার মান বজায় রাখতে বাধ্য করে।

---

### 🧠 উদাহরণ:

```sql
-- dept_id 3 is not available in departments
INSERT INTO students (name, dept_id) VALUES ('Hasan', 3); -- ❌ Error

-- First insert into parent
INSERT INTO departments (dept_name) VALUES ('BBA');

-- Now insert student with that dept
INSERT INTO students (name, dept_id) VALUES ('Hasan', 3); -- ✅ Now works
```

---

## 📝 সংক্ষেপে:

| বিষয়                  | ব্যাখ্যা                                            |
| --------------------- | --------------------------------------------------- |
| `FOREIGN KEY`         | অন্য টেবিলের প্রাইমারি কী রেফার করে                 |
| Referential Integrity | টেবিলের সম্পর্ক বজায় রাখে (সঠিক dept\_id থাকতে হবে) |

---



---


---

## 🟩 **Topic 5: Referential Integrity - Behaviors During Data Deletion**

### 🔶 সংজ্ঞা:

যখন আপনি একটি Parent টেবিল থেকে কোনো রেকর্ড **ডিলিট (DELETE)** করতে চান, এবং সেই রেকর্ডের সাথে অন্য কোনো টেবিলের Foreign Key দ্বারা সম্পর্কিত ডেটা থাকে, তখন PostgreSQL আপনাকে বাধা দিতে পারে, বা বিভিন্নভাবে আচরণ করতে পারে।

এটাই হচ্ছে **Referential Integrity during Delete**।

---

## 🎯 গুরুত্বপূর্ণ কনসেপ্ট: DELETE করার সময় ৪ ধরনের behavior থাকতে পারে

| অপশন                  | কী করে                                                    |
| --------------------- | --------------------------------------------------------- |
| `ON DELETE RESTRICT`  | যদি সম্পর্ক থাকে, ডিলিট করতে দেবে না                      |
| `ON DELETE CASCADE`   | Parent ডিলিট হলে, Child টাও অটোমেটিক ডিলিট হবে            |
| `ON DELETE SET NULL`  | Parent ডিলিট হলে, Child-এর Foreign Key কলাম null হয়ে যাবে |
| `ON DELETE NO ACTION` | Default। যদি সম্পর্ক থাকে, Error দিবে (Restrict-এর মতই)   |

---

## 🧠 উদাহরণ:

### 🔸 Step 1: Parent টেবিল (departments)

```sql
CREATE TABLE departments (
  dept_id SERIAL PRIMARY KEY,
  dept_name VARCHAR(100)
);
```

### 🔸 Step 2: Child টেবিল (students) with `ON DELETE CASCADE`

```sql
CREATE TABLE students (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100),
  dept_id INT,
  FOREIGN KEY (dept_id) REFERENCES departments(dept_id) ON DELETE CASCADE
);
```

---

### 🔸 Step 3: ডেটা ইনসার্ট

```sql
-- Departments
INSERT INTO departments (dept_name) VALUES ('CSE'), ('BBA');

-- Students
INSERT INTO students (name, dept_id) VALUES 
('Affnan', 1),
('Rakib', 1),
('Nusrat', 2);
```

---

### 🔸 Step 4: এখন Parent ডিলিট করবো

```sql
DELETE FROM departments WHERE dept_id = 1;
```

**ফলাফল:**
CSE ডিপার্টমেন্ট (dept\_id = 1) ডিলিট হলে, সেই ডিপার্টমেন্টের সব স্টুডেন্টও ডিলিট হয়ে যাবে (CASCADE এর কারণে)। শুধু Nusrat থাকবে।

---

## ✅ অন্য অপশনগুলো কিভাবে ব্যবহার করবো?

### 🔸 `ON DELETE SET NULL`:

```sql
FOREIGN KEY (dept_id) REFERENCES departments(dept_id) ON DELETE SET NULL
```

এক্ষেত্রে Parent ডিলিট হলে, student টেবিলে dept\_id `NULL` হয়ে যাবে।

### 🔸 `ON DELETE RESTRICT`:

```sql
FOREIGN KEY (dept_id) REFERENCES departments(dept_id) ON DELETE RESTRICT
```

Parent ডিলিট করতে পারবে না, যতক্ষণ child টেবিলে ঐ dept\_id আছে।

---

## 🔚 সারাংশ:

| অপশন                     | কি হয়?                                      |
| ------------------------ | ------------------------------------------- |
| `CASCADE`                | Parent ডিলিট হলে Child অটোমেটিক ডিলিট হয়    |
| `SET NULL`               | Parent ডিলিট হলে Child এর FK `NULL` হয়ে যায় |
| `RESTRICT` / `NO ACTION` | সম্পর্ক থাকলে Parent ডিলিট করা যায় না       |

---


---

## ✅ **50-6: INNER JOIN**

---

## 🟩 **Topic 6: INNER JOIN – দুটি টেবিলের সম্পর্কিত ডেটা একসাথে দেখানো**

### 🔶 সংজ্ঞা:

`INNER JOIN` ব্যবহার করা হয় **দুটি (বা তার বেশি) টেবিলের মধ্যে মিল পাওয়া রেকর্ডগুলোকে একসাথে দেখানোর জন্য**।
যেসব রেকর্ডে **matching condition (যেমন foreign key)** মেলে, শুধু সেই রেকর্ডগুলোই দেখানো হয়।

---

## 🔧 Syntax:

```sql
SELECT column_list
FROM table1
INNER JOIN table2
ON table1.common_column = table2.common_column;
```

---

## 🧠 উদাহরণ:

### 🔸 Step 1: Departments টেবিল (Parent Table)

```sql
CREATE TABLE departments (
  dept_id SERIAL PRIMARY KEY,
  dept_name VARCHAR(100)
);
```

### 🔸 Step 2: Students টেবিল (Child Table)

```sql
CREATE TABLE students (
  id SERIAL PRIMARY KEY,
  name VARCHAR(100),
  dept_id INT,
  FOREIGN KEY (dept_id) REFERENCES departments(dept_id)
);
```

---

### 🔸 Step 3: কিছু ডেটা ইনসার্ট করি

```sql
-- Departments
INSERT INTO departments (dept_name) VALUES ('CSE'), ('EEE'), ('BBA');

-- Students
INSERT INTO students (name, dept_id) VALUES 
('Affnan', 1),
('Nusrat', 1),
('Rakib', 2),
('Mitu', NULL);
```

---

### 🔸 Step 4: INNER JOIN করে দেখা

```sql
SELECT students.name AS student_name, departments.dept_name AS department
FROM students
INNER JOIN departments
ON students.dept_id = departments.dept_id;
```

---

### 🔍 ফলাফল:

| student\_name | department |
| ------------- | ---------- |
| Affnan        | CSE        |
| Nusrat        | CSE        |
| Rakib         | EEE        |

**Note:**

* এখানে **Mitu** দেখানো হয়নি কারণ তার `dept_id` NULL → কোনো match নাই → তাই exclude হয়েছে।
* INNER JOIN শুধুমাত্র **matching value** থাকলেই দেখায়।

---

## ✅ সংক্ষেপে মনে রাখার কৌশল:

**INNER JOIN = যেসব রেকর্ড দুই টেবিলে মিলে, শুধু সেগুলো দেখাও**

---



## ✅ **50-7: LEFT JOIN & RIGHT JOIN**

ভালো! আমরা এখন PostgreSQL-এর **Topic 6: Joining Tables with INNER JOIN** শেষ করেছি।

এখন আসি 👉

---

## 🟪 **Topic 7: Understanding Left and Right Joins**

### 🔹 ১. LEFT JOIN কী?

**LEFT JOIN** এমন একটি JOIN যেটি **বাম পাশে (Left Table)** যেসব ডেটা আছে, **সবগুলোই দেখায়**, এবং ডান পাশে মিল না থাকলে **NULL দেখায়**।

---

### ✅ Syntax:

```sql
SELECT *
FROM students
LEFT JOIN departments
ON students.dept_id = departments.dept_id;
```

---

### 📘 ধরো তোমার দুটি টেবিল:

#### 🔸 `students` টেবিল:

| id | name   | dept\_id |
| -- | ------ | -------- |
| 1  | Affnan | 1        |
| 2  | Nusrat | 1        |
| 3  | Rakib  | 2        |
| 4  | Mitu   | NULL     |

#### 🔸 `departments` টেবিল:

| dept\_id | dept\_name |
| -------- | ---------- |
| 1        | CSE        |
| 2        | EEE        |

---

### 🧾 এখন যদি আমরা এই কুয়েরি চালাই:

```sql
SELECT students.name, departments.dept_name
FROM students
LEFT JOIN departments
ON students.dept_id = departments.dept_id;
```

### 🔍 ফলাফল হবে:

| name   | dept\_name |
| ------ | ---------- |
| Affnan | CSE        |
| Nusrat | CSE        |
| Rakib  | EEE        |
| Mitu   | NULL       |

> 🔑 কারণ `Mitu`-র কোনো `dept_id` নেই (NULL), তাই ডান পাশে মিল পাওয়া যায়নি — কিন্তু `LEFT JOIN` হবার কারণে `Mitu` কে দেখিয়েছে, আর `dept_name` হিসেবে `NULL`।

---

### 🔹 ২. RIGHT JOIN কী?

**RIGHT JOIN** হলো উল্টো — **ডান পাশে (Right Table)** যেসব ডেটা আছে, **সবগুলোই দেখায়**, বাম পাশে মিল না থাকলে **NULL দেখায়**।

---

### ✅ Syntax:

```sql
SELECT *
FROM students
RIGHT JOIN departments
ON students.dept_id = departments.dept_id;
```

---

### ✨ ধরো departments টেবিলে আরেকটা ডিপার্টমেন্ট আছে, যেটিতে কোনো student নাই:

| dept\_id | dept\_name |
| -------- | ---------- |
| 1        | CSE        |
| 2        | EEE        |
| 3        | BBA        |

তখন RIGHT JOIN দিলে:

| name   | dept\_name |
| ------ | ---------- |
| Affnan | CSE        |
| Nusrat | CSE        |
| Rakib  | EEE        |
| NULL   | BBA        |

> 🔑 কারণ BBA ডিপার্টমেন্টে কোনো স্টুডেন্ট নেই, তবুও **RIGHT JOIN** এটা দেখিয়েছে।

---

## 📌 সংক্ষেপে মনে রাখো:

| JOIN Type  | দেখাবে কোনটা সব | না মেললে |
| ---------- | --------------- | -------- |
| INNER JOIN | শুধু মিল থাকলে  | বাদ যাবে |
| LEFT JOIN  | বাম পাশ সব      | NULL হবে |
| RIGHT JOIN | ডান পাশ সব      | NULL হবে |

---


---

## ✅ **50-8: FULL JOIN, CROSS JOIN, NATURAL JOIN**


---

## 🟪 **FULL JOIN (FULL OUTER JOIN)**

### 🔹 কী এটা?

**FULL JOIN** দুই পাশে (LEFT + RIGHT) যেসব ডেটা আছে, **সব দেখায়**। যেগুলো মিলে না, সেখানে **NULL** দেয়।

---

### ✅ Syntax:

```sql
SELECT *
FROM students
FULL JOIN departments
ON students.dept_id = departments.dept_id;
```

---

### 📘 উদাহরণ:

`students` টেবিলে ৪ জন স্টুডেন্ট, যার একজনের dept\_id নাই,
`departments` টেবিলে ৩টা ডিপার্টমেন্ট, যার একটিতে কোনো student নাই।

**FULL JOIN চালালে:**

| name   | dept\_name |
| ------ | ---------- |
| Affnan | CSE        |
| Nusrat | CSE        |
| Rakib  | EEE        |
| Mitu   | NULL       |
| NULL   | BBA        |

> 🔑 কারণ `Mitu`-র কোনো department নাই, আর `BBA` department-এ কোনো student নাই — FULL JOIN দুপক্ষই দেখায়।

---

## 🟪 **CROSS JOIN**

### 🔹 কী এটা?

**CROSS JOIN** দুই টেবিলের **প্রতিটি রেকর্ডের সাথে অন্য টেবিলের প্রতিটি রেকর্ড** কে **মিলায়**, অর্থাৎ কার্টেশিয়ান প্রোডাক্ট তৈরি করে।

---

### ✅ Syntax:

```sql
SELECT *
FROM students
CROSS JOIN departments;
```

---

### 📘 উদাহরণ:

* যদি `students` টেবিলে 3 জন থাকে
* আর `departments` টেবিলে 2টা ডিপার্টমেন্ট থাকে

তাহলে **3 x 2 = 6 রেকর্ড** রিটার্ন করবে।

| name   | dept\_name |
| ------ | ---------- |
| Affnan | CSE        |
| Affnan | EEE        |
| Nusrat | CSE        |
| Nusrat | EEE        |
| Rakib  | CSE        |
| Rakib  | EEE        |

> 🔑 কারণ সবাই সবার সাথে একবার করে জোড়া হয়।

⚠️ এটা সাধারণত **testing purposes** বা **combinations** খুঁজতে ব্যবহার করা হয়।

---

## 🟪 **NATURAL JOIN**

### 🔹 কী এটা?

**NATURAL JOIN** এমন JOIN যেখানে দুই টেবিলের **একই নাম ও ডেটাটাইপের কলাম** স্বয়ংক্রিয়ভাবে **match** করা হয়।

---

### ✅ Syntax:

```sql
SELECT *
FROM students
NATURAL JOIN departments;
```

> শর্ত: `students` এবং `departments` টেবিলে যদি **একই নামের কলাম** থাকে (যেমন: `dept_id`), তখনই কাজ করবে।

---

### 📘 ধরো:

```sql
students: id, name, dept_id  
departments: dept_id, dept_name  
```

তখন NATURAL JOIN এমনভাবে কাজ করবে যেন তুমি লিখছো:

```sql
ON students.dept_id = departments.dept_id
```

---

### ⚠️ সাবধানতা:

* NATURAL JOIN নিজে নিজে মেলানো চেষ্টা করে
* তাই সবসময় বুঝে ব্যবহার করো, ভুল JOIN হতে পারে

---

## 🧠 সংক্ষেপে পার্থক্য:

| JOIN টাইপ    | কাজ করে কিভাবে                          |
| ------------ | --------------------------------------- |
| FULL JOIN    | দুপক্ষের সব ডেটা দেখায়                  |
| CROSS JOIN   | প্রতিটি রেকর্ড সবার সাথে কম্বিনেশন করে  |
| NATURAL JOIN | একই নাম ও টাইপের কলাম দিয়ে অটো JOIN করে |

---

## ✅ **50-9: Pagination with LIMIT OFFSET & DELETE**


---

## 🟨 **1. Pagination using LIMIT and OFFSET**

### 🔹 কেন ব্যবহার করি?

যখন ডেটা অনেক বেশি হয় (যেমন: ১০০০টা row), তখন সব একসাথে না দেখিয়ে **প্রতি পেজে কিছু সংখ্যক দেখাতে চাই**। তখনই `LIMIT` এবং `OFFSET` ব্যবহার করি।

---

### ✅ Syntax:

```sql
SELECT * FROM students
LIMIT 5 OFFSET 0;
```

---

### 🔍 ব্যাখ্যা:

* `LIMIT 5` মানে → **শুধু ৫টা row দেখাবে**
* `OFFSET 0` মানে → **শুরু করবে প্রথম row থেকে**

---

### 📘 উদাহরণ:

```sql
-- Page 1
SELECT * FROM students
LIMIT 5 OFFSET 0;

-- Page 2
SELECT * FROM students
LIMIT 5 OFFSET 5;

-- Page 3
SELECT * FROM students
LIMIT 5 OFFSET 10;
```

> 🔁 এইভাবে তুমি Pagination করতে পারো — প্রতি পেজে ৫টি রেকর্ড।

---

## 🟨 **2. DELETE Statement in PostgreSQL**

### 🔹 কাজ কী?

ডেটাবেজ থেকে একটি বা একাধিক row **permanently মুছে ফেলার জন্য** `DELETE` ব্যবহার করি।

---

### ✅ Syntax:

```sql
DELETE FROM students
WHERE id = 3;
```

---

### ⚠️ সতর্কতা:

`WHERE` ক্লজ না দিলে → **পুরো টেবিলের সব row মুছে যাবে!**

```sql
DELETE FROM students; -- সব data চলে যাবে!
```

---

### 📘 উদাহরণ:

```sql
-- নাম দিয়ে মুছো
DELETE FROM students
WHERE name = 'Rakibul Islam';

-- বয়স ১৮ এর নিচে যারা, তাদের মুছো
DELETE FROM students
WHERE age < 18;
```

---

## 🔄 Pagination + DELETE Practical Example:

ধরো তুমি `students` টেবিল দেখাচ্ছো প্রতি পেজে ৫টি করে, এবং ইউজার একটাকে delete করতে চায়।

```sql
-- দেখাও:
SELECT * FROM students
LIMIT 5 OFFSET 0;

-- তারপর মুছো:
DELETE FROM students
WHERE id = 2;
```

---

## ✅ সংক্ষেপে মনে রাখার টিপস:

| কাজ        | SQL                           |
| ---------- | ----------------------------- |
| Pagination | `LIMIT 10 OFFSET 20`          |
| DELETE Row | `DELETE FROM table WHERE ...` |

---

| ID | Name   |
| -- | ------ |
| 1  | Affnan |
| 2  | Nusrat |
| 3  | Mehedi |
| 4  | Sadia  |
| 5  | Rakib  |
| 6  | Mamdud |
| 7  | Rayhan |

-- Page 1:
SELECT * FROM students LIMIT 3 OFFSET 0;
-- দেখাবে: Affnan, Nusrat, Mehedi

-- Page 2:
SELECT * FROM students LIMIT 3 OFFSET 3;
-- দেখাবে: Sadia, Rakib, Mamdud

-- Page 3:
SELECT * FROM students LIMIT 3 OFFSET 6;
-- দেখাবে: Rayhan

OFFSET = কতগুলো row স্কিপ করবে
LIMIT  = কতগুলো row দেখাবে


---

## ✅ **50-10: UPDATE Operator**

### ✔ Example:

```sql
UPDATE students
SET age = 21
WHERE name = 'Affnan Sawad';
```


---

## ✅ 51-2: **Subqueries কী? (সাবকুয়েরি)**

**Subquery** মানে হচ্ছে – একটি কুয়েরির (query) ভিতরে আরেকটি কুয়েরি। এটা তখন ব্যবহার হয় যখন বাইরের কুয়েরির জন্য ভিতরের কুয়েরির ফলাফল দরকার।

### 🟢 উদাহরণ:

```sql
-- এমন সব কর্মচারীর নাম বের করো যাদের বেতন গড় বেতনের চেয়ে বেশি
SELECT name, salary
FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```

🔹 এখানে `(SELECT AVG(salary)...` হলো **subquery**
🔹 এটা `WHERE` ক্লজে ব্যবহার হয়েছে।

---

## ✅ 51-3: **Subqueries কোথায় কোথায় ব্যবহার হয়?**

Subquery নিচের জায়গাগুলোতে ব্যবহার হয়:

### 1. `WHERE` ক্লজে:

```sql
SELECT name FROM students
WHERE marks > (SELECT AVG(marks) FROM students);
```

### 2. `FROM` ক্লজে:

```sql
SELECT avg_salary FROM (SELECT AVG(salary) AS avg_salary FROM employees) AS sub;
```

### 3. `SELECT` ক্লজে:

```sql
SELECT name, (SELECT COUNT(*) FROM orders WHERE customer_id = customers.id) AS order_count
FROM customers;
```

🔸 এটা Nested Query বা Inline Query বলেও ডাকা হয়।

---

## ✅ 51-4: **Views কী? (ভিউ)**

**View** হলো virtual table। এটি একটি কুয়েরি, যেটা আপনি table-এর মতো ব্যবহার করতে পারেন। এটা ডেটা নিরাপত্তা এবং রিইউজেবল কুয়েরির জন্য ব্যবহৃত হয়।

### 🟢 উদাহরণ:

```sql
CREATE VIEW high_salary_employees AS
SELECT name, salary FROM employees WHERE salary > 50000;

-- এরপর view ব্যবহার করে:
SELECT * FROM high_salary_employees;
```

🔹 View এর ভিতরে ডেটা থাকে না, কুয়েরি স্টোর হয়।

---

## ✅ 51-5: **Functions in PostgreSQL (ফাংশন)**

Function হচ্ছে – একটি reusable code block যেটা আপনি বারবার চালাতে পারেন। এটি ইনপুট নেয়, কিছু প্রসেস করে, রেজাল্ট রিটার্ন করে।

### 🟢 উদাহরণ:

```sql
CREATE FUNCTION get_discount(price numeric) RETURNS numeric AS $$
BEGIN
  RETURN price * 0.90; -- 10% discount
END;
$$ LANGUAGE plpgsql;

-- Use:
SELECT get_discount(1000); -- ফলাফল: 900
```

---

## ✅ 51-6: **Stored Procedure (স্টোরড প্রসিডিউর)**

**Procedure** হলো function-এর মতো, কিন্তু এটা সাধারণত **action** (যেমন insert, update) করে এবং return করতে না-ও পারে।

### 🟢 উদাহরণ:

```sql
CREATE PROCEDURE insert_student(name text, marks int)
LANGUAGE plpgsql
AS $$
BEGIN
  INSERT INTO students(name, marks) VALUES (name, marks);
END;
$$;

-- কল করতে:
CALL insert_student('Affnan', 90);
```

---

## ✅ 51-7: **Triggers (ট্রিগার)**

Trigger এমন কোড যেটা **অটোমেটিক** চলে যায় যখন কোনো ঘটনা ঘটে (যেমন INSERT/UPDATE/DELETE)।

### 🟢 উদাহরণ:

```sql
-- Audit টেবিলে INSERT হলেই অন্য টেবিলে লোগ রাখবে

CREATE TABLE audit_log(id serial, action_time timestamp);

CREATE FUNCTION log_insert() RETURNS trigger AS $$
BEGIN
  INSERT INTO audit_log(action_time) VALUES (now());
  RETURN NEW;
END;
$$ LANGUAGE plpgsql;

CREATE TRIGGER trigger_log
AFTER INSERT ON employees
FOR EACH ROW EXECUTE FUNCTION log_insert();
```

---

## ✅ 51-8: **Indexing Techniques in PostgreSQL**

**Index** হচ্ছে একটা বিশেষ data structure (যেমন B-Tree), যা সার্চ ও কোয়েরি ফাস্ট করে।

### 🟢 উদাহরণ:

```sql
-- নাম ফিল্ডে ইনডেক্স তৈরি করো
CREATE INDEX idx_name ON employees(name);
```

🔹 এতে `WHERE name = 'Affnan'` টাইপের কুয়েরি অনেক দ্রুত হবে।

---

## ✅ 51-9: **Index কিভাবে কাজ করে?**

📌 সাধারণত, PostgreSQL **B-Tree Index** ব্যবহার করে। এটি binary search-এর মতো কাজ করে, যেটা `O(log n)` টাইমে সার্চ করে।

### 🔍 উদাহরণ:

**Table:** 10 লাখ ডেটা আছে।

কুয়েরি:

```
SELECT * FROM employees WHERE name = 'Affnan';
````



------------------------------

This is the Basics to Intermidiate Level of DBMS ( PostgreSQL  ) .


------------------------------------










