---

# 🌟 Day 5 – Apex Introduction (Salesforce)

---

## 🚀 1. What is Apex?

**Apex** is a **programming language developed by Salesforce** that allows developers to write **custom logic and automation** on the Salesforce platform.

👉 It is similar to Java and is used when:

* Flow Builder is not enough
* Complex business logic is required
* Integration with external systems is needed

💡 **In simple words:**
Apex = *Coding power of Salesforce*

---

## ⚖️ 2. Difference

### 🔄 Flow vs Apex

| 🔧 Flow Builder           | 💻 Apex                        |
| ------------------------- | ------------------------------ |
| No-code / Low-code        | Full coding required           |
| Drag-and-drop UI          | Write logic manually           |
| Easy to use               | Requires programming knowledge |
| Limited for complex logic | Handles complex scenarios      |
| Quick automation          | Powerful customization         |

---

### ⚙️ Configuration vs Coding

| ⚙️ Configuration           | 💻 Coding                 |
| -------------------------- | ------------------------- |
| Done using UI tools        | Done using programming    |
| Faster to build            | Takes more time           |
| Less flexible              | Highly flexible           |
| Limited logic              | Advanced logic possible   |
| No technical skills needed | Requires developer skills |

💡 **Summary:**
👉 Use *Configuration first* → then use *Apex if needed*

---

## 💡 3. Real Examples Where Apex Is Needed

### 1️⃣ Complex Calculations

* Calculate student grades based on multiple conditions
* Apply different weightages dynamically

---

### 2️⃣ External System Integration

* Connect Salesforce with payment systems or portals
* Send/receive data using APIs

---

### 3️⃣ Advanced Automation

* Trigger logic across multiple objects
* Perform bulk operations efficiently

---

## 🏫 4. Integrated System Design – College Management System

Let’s design a **College Management System** using Salesforce 👇

---

### 🧩 CRM (Customer Relationship Management)

* Students = Customers
* Faculty = Internal users
* Courses = Services
* Helps manage student data and interactions

---

### 📦 Objects

* **Student__c**
* **Course__c**
* **Faculty__c**
* **Enrollment__c**

---

### 🔗 Relationships

* Student → Enrollment (1 to many)
* Course → Enrollment (1 to many)
* Faculty → Course (1 to many)

💡 Enrollment acts as a bridge between Student and Course

---

### ✅ Validation

* Email must be valid format
* Student age > 17
* Course capacity should not exceed limit

👉 Prevents incorrect data entry

---

### 🔄 Flow

* Auto-create enrollment when student selects course
* Send email notification after registration
* Update course status automatically

👉 Used for simple automation

---

### 💻 Apex

* Calculate GPA automatically
* Assign faculty based on workload
* Handle bulk student enrollment

👉 Used for complex logic

---

## 🧠 5. Pseudocode Examples

### 📌 Example 1: GPA Calculation

```id="ps1"
IF marks >= 90 → Grade = A
ELSE IF marks >= 75 → Grade = B
ELSE → Grade = C
```

---

### 📌 Example 2: Auto Enrollment

```id="ps2"
WHEN student selects course
CHECK course capacity
IF seats available
   CREATE enrollment
ELSE
   SHOW error
```

---

### 📌 Example 3: Faculty Assignment

```id="ps3"
FOR each faculty
   CHECK workload
ASSIGN course to least busy faculty
```

---

## 🧠 6. Reflection – Why Enterprise Systems Need Programming

In real-world applications:

✨ Business logic becomes complex
✨ Data volume increases
✨ Integrations are required
✨ Automation needs flexibility

👉 Tools like Flow are powerful but limited
👉 Apex helps handle advanced requirements

---

## 🎯 Conclusion

Apex adds **power, flexibility, and scalability** to Salesforce.

✔ Use Flow for simple tasks
✔ Use Apex for complex logic

👉 Together, they create a **complete and efficient system**

---