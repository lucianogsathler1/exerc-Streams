# Java Streams & File Processing Exercise

## 📋 Overview
This project is a practical implementation focused on practicing **Java Streams API**, **Lambda Expressions**, and **File I/O operations** (`BufferedReader`/`FileReader`). It reads data from a comma-separated values (CSV) file, populates a custom domain model, and executes advanced data processing queries.

---

## 🚀 Key Features & Concepts Applied
* **File Handling:** Efficient reading of text files using `BufferedReader` and `FileReader`.
* **Object-Oriented Modeling:** Clean domain design with an `Employee` entity encapsulating state and behavior.
* **Java Streams & Functional Programming:**
  * `.filter()`: Conditional extraction of records.
  * `.map()`: Data transformation and projection.
  * `.sorted()`: Stream ordering.
  * `.collect()`: Terminal operations using `Collectors.toList()`.
  * `.reduce()`: Aggregation operations (such as summing salaries).
* **Robust Input Handling:** Configured `Locale.US` to ensure consistent decimal number parsing regardless of the operating system's regional settings.

---

## 🛠️ Technologies Used
* **Java** (JDK 17+)
* **Maven** (Dependency & Project Management)
* **IntelliJ IDEA**

---

## 💻 Code Highlights (Stream Processing Example)

```java
// Filtering employees above a certain salary threshold, extracting their emails in alphabetical order
List<String> emails = list.stream()
        .filter(x -> x.getSalary() > salary)
        .map(x -> x.getEmail())
        .sorted()
        .collect(Collectors.toList());
