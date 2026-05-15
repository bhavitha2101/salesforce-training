# 📘 Day 3 – Data Modeling in Salesforce

## 🌟 Introduction

Data modeling is the foundation of every enterprise application.
In Salesforce, data is organized using apps, objects, records, and fields to manage business information efficiently.

This project demonstrates:

* Core Salesforce data modeling concepts
* Standard vs Custom Objects
* College Data Model
* Formula Fields
* Validation Rules
* Importance of structured enterprise data

---

1. 🧩 *Difference Between App, Object, Record, and Field*

| Concept   | Description                                                               | Example                   |
| --------- | ------------------------------------------------------------------------- | ------------------------- |
| 📱 App    | A collection of tools, tabs, and features designed for a business process | Sales App                 |
| 📦 Object | A database table that stores related data                                 | Student Object            |
| 📝 Record | A single row/data entry inside an object                                  | One student’s information |
| 🏷️ Field | A column that stores a specific type of information                       | Student Name, Roll Number |

---

2. ⚖️ *Standard Objects vs Custom Objects*

| Standard Objects                        | Custom Objects                       |
| --------------------------------------- | ------------------------------------ |
| Pre-built by Salesforce                 | Created by users/admins              |
| Used for common business needs          | Used for organization-specific needs |
| Examples: Account, Contact, Opportunity | Examples: Student, Course, Library   |
| Cannot be deleted                       | Can be modified or deleted           |

## ✅ Examples

### Standard Objects

* Account
* Contact
* Opportunity
* Lead

### Custom Objects

* Student
* Faculty
* Attendance
* Course

---

3. 🎓 *College Data Model*

## 📚 Objects Used

| Object Name | Purpose                       |
| ----------- | ----------------------------- |
| Student     | Stores student details        |
| Faculty     | Stores faculty information    |
| Course      | Stores course details         |
| Attendance  | Tracks attendance             |
| Department  | Stores department information |

---

## 🔗 Relationships

| Parent Object | Child Object | Relationship Type |
| ------------- | ------------ | ----------------- |
| Department    | Student      | Lookup            |
| Department    | Faculty      | Lookup            |
| Faculty       | Course       | Master-Detail     |
| Student       | Attendance   | Master-Detail     |
| Course        | Attendance   | Lookup            |

---

# 🖼️ College Data Model Diagram

```text
Department
   │
   ├── Student
   │      │
   │      └── Attendance
   │
   └── Faculty
           │
           └── Course
```

---

4. 🧮 *Formula Fields*

Formula fields automatically calculate values based on other fields.

## ✅ Example 1: Student Percentage

### Formula

```text
(Total_Marks__c / Maximum_Marks__c) * 100
```

### Purpose

Calculates the student’s percentage automatically.

---

## ✅ Example 2: Days Remaining for Fee Payment

### Formula

```text
Due_Date__c - TODAY()
```

### Purpose

Shows how many days are left before fee payment deadline.

---

## ✅ Advantages of Formula Fields

* Reduces manual calculations
* Improves accuracy
* Updates automatically
* Saves time

---

5. *Validation Rules*

Validation rules ensure only valid data is entered into Salesforce.

---

## ✅ Example 1: Phone Number Validation

### Rule

Phone number must contain exactly 10 digits.

### Formula

```text
LEN(Phone__c) <> 10
```

### Error Message

```text
Phone number must be 10 digits.
```

---

## ✅ Example 2: Student Age Validation

### Rule

Student age must be greater than 17.

### Formula

```text
Age__c < 18
```

### Error Message

```text
Student must be at least 18 years old.
```

---

## 🎯 Benefits of Validation Rules

* Prevents incorrect data entry
* Maintains data quality
* Improves reliability
* Reduces duplicate and invalid records

---
6. *Reflections*
# 💡 Why Structured Enterprise Data Matters

Structured enterprise data is extremely important because organizations handle huge amounts of information every day.

Well-structured data helps businesses:

* 📊 Make better decisions
* ⚡ Improve productivity
* 🔍 Find information quickly
* 🤝 Improve customer relationships
* 🔐 Maintain data accuracy and security

In Salesforce, proper data modeling ensures:

* Better automation
* Efficient reporting
* Easy scalability
* High-quality business processes

Without structured data, systems become confusing, slow, and difficult to manage.

---

# 🚀 Conclusion

This project helped in understanding:

* Salesforce data modeling concepts
* Objects and relationships
* Formula fields
* Validation rules
* Importance of organized enterprise data

Data modeling is the backbone of scalable and efficient Salesforce applications.

---

# 🛠️ Technologies Used

* Salesforce CRM
* Salesforce Objects & Relationships
* Formula Fields
* Validation Rules
* Schema Builder

---


