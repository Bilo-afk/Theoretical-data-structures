# 📘 — Arrays & Recursion
*(النسخة الثنائية: English + العربية)*

---

## 🇬🇧 **English Section**

### 🧠 1. What is an Array?
An **array** is like an egg carton — it holds several values of the **same type**, stored **next to each other** in memory.  
Each value has a number called an **index**, starting from 0.

| Index | Value |
|--------|--------|
| 0 | 5 |
| 1 | 7 |
| 2 | 9 |
| 3 | 4 |

The first element is at index 0, and the last is at index 3.

---

### 💾 2. Why Use Arrays?
Instead of creating 10 separate variables like this:
```cpp
int s1, s2, s3, s4, s5, s6, s7, s8, s9, s10;
```
We can use one array:
```cpp
int scores[10];
```
Arrays make it easier to manage large amounts of data efficiently.

---

### 🧩 3. Memory Layout
Arrays are stored in **contiguous memory**.  
If the first element’s address is 1000 and each integer takes 4 bytes:
- `arr[0] → 1000`  
- `arr[1] → 1004`  
- `arr[2] → 1008`  

That’s why accessing any element by index is **O(1)** time (constant).

---

### ⚙️ 4. Common Array Operations
1. Insert or initialize elements  
2. Access by index  
3. Modify a value  
4. Search for an element  
5. Copy or merge arrays  
6. Sort or reverse elements  

---

### 🚧 5. Array Limitations
Arrays have a **fixed size**.  
You can’t make them grow or shrink dynamically — for that, use `std::vector` in C++.

---

### 🔁 6. What is Recursion?
**Recursion** means a function that **calls itself** to solve a smaller version of the same problem.  
It continues calling itself until it reaches a **Base Case** — a stopping condition.

Example idea:
> To find 4! = 4 × 3!  
> And 3! = 3 × 2!  
> And 2! = 2 × 1!  
> Stop when you reach 1! = 1  

---

### 🧮 7. Structure of a Recursive Function
- **Base Case:** when to stop  
- **Recursive Case:** when to keep calling itself  

Without a base case → infinite recursion → program crash (stack overflow 💥).

---

### 🧭 8. Loop vs Recursion

| Comparison | Loop | Recursion |
|-------------|-------|------------|
| Execution | Repeats inside same block | Function calls itself |
| Memory | Low usage | Uses stack memory |
| Speed | Usually faster | Usually slower |
| Readability | Sometimes complex | Easier for some problems |
| Stop condition | Loop condition | Base case |

---

### 💡 9. Real-Life Examples
- Cooking: “Repeat the same steps for each layer.”  
- Mirrors facing each other: Infinite reflection.  
- Countdown: Decrease one number each time until 0.

---

### 🏁 10. Summary
- Arrays: fixed-size collections of elements stored consecutively.  
- Recursion: a function that calls itself to solve smaller subproblems.  
- Both are essential for advanced data structures like trees, sorting, and searching.

---

## 🇸🇦 **القسم العربي**

### 🧠 1. ما هي المصفوفة (Array)؟
المصفوفة مثل **علبة بيض** فيها خانات متجاورة، كل خانة فيها قيمة من **نفس النوع**،  
ولكل خانة رقم خاص اسمه **الفهرس (Index)** يبدأ من الصفر.

| الفهرس | القيمة |
|---------|---------|
| 0 | 5 |
| 1 | 7 |
| 2 | 9 |
| 3 | 4 |

---

### 💾 2. لماذا نستخدم المصفوفات؟
بدل ما نكتب 10 متغيرات:
```cpp
int s1, s2, s3, s4, s5, s6, s7, s8, s9, s10;
```
نقدر نكتب:
```cpp
int scores[10];
```
فتصير البيانات منظمة وسهلة التعامل بحلقات `for`.

---

### 🧩 3. تخزين المصفوفة في الذاكرة
تُخزّن العناصر **جنب بعض** في الذاكرة.  
إذا كان أول عنوان 1000 ونوع البيانات `int` (4 بايت):
- العنصر [0] → 1000  
- العنصر [1] → 1004  
- العنصر [2] → 1008  

لذلك الوصول لأي عنصر يكون بسرعة **O(1)**.

---

### ⚙️ 4. العمليات الأساسية على المصفوفة
1. إدخال القيم  
2. الوصول إلى عنصر  
3. تعديل قيمة  
4. البحث  
5. النسخ أو الدمج  
6. الترتيب أو العكس  

---

### 🚧 5. حدود المصفوفة
المصفوفة **ثابتة الحجم**.  
لا يمكن تغيير حجمها بعد إنشائها، لذلك نستخدم `vector` عند الحاجة إلى المرونة.

---

### 🔁 6. ما هي العودية (Recursion)؟
العودية هي أن **الدالة تستدعي نفسها** لحل نفس المشكلة بخطوات أصغر.  
لكن لازم نحدد **حالة توقف (Base Case)**، وإلا ستكرر نفسها للأبد!

---

### 🧮 7. تركيب الدالة العودية
1. **الحالة الأساسية:** الشرط الذي نوقف عنده.  
2. **الحالة التكرارية:** الجزء الذي يستدعي نفسه من جديد.

بدون الحالة الأساسية → خطأ Stack Overflow ⚠️

---

### 🧭 8. الفرق بين الحلقة والعودية

| المقارنة | الحلقة | العودية |
|-----------|----------|-----------|
| طريقة التنفيذ | تكرار داخل نفس الدالة | الدالة تستدعي نفسها |
| الذاكرة | قليلة | تستهلك أكثر |
| السرعة | أسرع عادة | أبطأ عادة |
| السهولة | أحيانًا معقدة | أحيانًا أوضح |
| التوقف | شرط في الحلقة | Base Case |

---

### 💡 9. أمثلة من الحياة
- الطبخ: “كرّر نفس الخطوات لكل طبقة.”  
- المرايا المتقابلة: انعكاس لا نهائي.  
- العد التنازلي: كل مرة تنقص رقم حتى تصل للصفر.

---

### 🏁 10. الخلاصة
- المصفوفة: مجموعة عناصر من نفس النوع متجاورة في الذاكرة.  
- العودية: دالة تستدعي نفسها لتبسيط المشكلة خطوة بخطوة.  
- كلتاهما أساسيتان في دراسة هياكل البيانات المتقدمة.
