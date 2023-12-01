## Regular Expressions in React

Regular expressions are a powerful tool for pattern matching and string manipulation. They are commonly used in React applications for tasks such as form validation, data filtering, and text processing.

Here are some commonly used regular expressions in React:

### Table of Contents

| No. | Regex |
|---|---|
| 1. | [Decimal Numbers Up to Two Decimal Places](#1-decimal-numbers-up-to-two-decimal-places) |
| 2. | [Decimal Numbers with Metric Unit Up to Three Decimals](#2-decimal-numbers-with-metric-unit-up-to-three-decimals) |
| 3. | [Decimal Numbers with Weight Unit Up to Three Decimals](#3-decimal-numbers-with-weight-unit-up-to-three-decimals) |
| 4. | [Decimal Numbers Up to Three Decimals](#4-decimal-numbers-up-to-three-decimals) |
| 5. | [Percentage Up to Two Decimals](#5-percentage-up-to-two-decimals) |

### 1. Decimal Numbers Up to Two Decimal Places

```javascript
const twoDecimal = /^\d+(\.[0-9]{0,2})?<span class="math-inline">/;
```
*This regular expression matches decimal numbers with up to two decimal places\. The \`\\d\+\` matches one or more digits, \`\\\.\` matches a literal dot, and \`\\\{0,2\\\}\` matches zero to two occurrences of the preceding character \(i\.e\., the dot\)\.*

---

### 2. Decimal Numbers with Metric Unit Up to Three Decimals

```javascript
const metricUnit \= /^\\d\+\(\\\.\[0\-9\]\{0,3\}\)?\(ml\|m\)?</span>/;
```
*This regular expression matches decimal numbers with an optional metric unit (ml or m) and up to three decimal places. The `\d+` matches one or more digits, `\.` matches a literal dot, `\{0,3\}` matches zero to three occurrences of the preceding character (i.e., the dot), and `(ml|m)?` matches zero or one occurrence of either "ml" or "m".*

---

### 3. Decimal Numbers with Weight Unit Up to Three Decimals

```javascript
const weightUnit = /^\d+(\.[0-9]{0,3})?(g|kg|k)?<span class="math-inline">/;
```
*This regular expression matches decimal numbers with an optional weight unit \(g, kg, or k\) and up to three decimal places\. The \`\\d\+\` matches one or more digits, \`\\\.\` matches a literal dot, \`\\\{0,3\\\}\` matches zero to three occurrences of the preceding character \(i\.e\., the dot\), and \`\(g\|kg\|k\)?\` matches zero or one occurrence of either "g", "kg", or "k"\.*

---

### 4. Decimal Numbers Up to Three Decimals
```javascript
const threeDecimal \= /^\\d\+\(\\\.\[0\-9\]\{0,3\}\)?</span>/;
```
*This regular expression matches decimal numbers with up to three decimal places. The `\d+` matches one or more digits, `\.` matches a literal dot, and `\{0,3\}` matches zero to three occurrences of the preceding character (i.e., the dot).*

---

### 5. Percentage Up to Two Decimals

```javascript
const percentage = /^(100(\.[0-9]{1,2})?|[1-9]?\d(\.[0-9]{1,2})?)|(^0)(\.[0-9]{1,2})%?$/;
```
*This regular expression matches percentages with up to two decimal places. The `^` matches the beginning of the string, `(100(\.[0-9]{1,2})?)` matches either "100" (for 100%) or "100" followed by a dot and one or two digits (for percentages between 100 and 101.99%), `|` matches an or operator, `[1-9]?\d(\.[0-9]{1,2})` matches one to nine digits (for percentages between 1 and 99) followed by a dot and one or two digits (for percentages between 0.1 and 99.99%), `|` matches an or operator, `(^0)` matches a literal zero at the beginning of the string, `(\.[0-9]{1,2})?` matches a dot followed by one or two digits (for percentages between 0.01 and 0.99), and `%?` matches either a percent sign (%) or an empty string (for 0%).*

---
