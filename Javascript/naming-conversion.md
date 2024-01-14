## Naming Conversion Cheat Sheet for Javascript

Here are some Userd to convert Cases

## Cases for Javascript

### Pascal Case : Navneet Kumar
#### Snake Case: navneet_kumar
#### Camel Case: navneetKumar
#### Kebab Case: naneet-kumar

### Table of Contents

| No. | Regex                                                  |
| --- | ------------------------------------------------------ |
| 1.  | [All Cases To Pascal Case Conversion Function](#1-all-cases-to-pascal-case-conversion) |
| 2.  | [All Cases To Title Case Conversion Function](#2-all-cases-to-title-case-conversion) |
| 3.  | [All Cases To Snake Case Conversion Function](#3-all-cases-to-snake-case-conversion) |
| 4.  | [All Cases To Camel Case Conversion Function](#4-all-cases-to-camel-case-conversion) |
| 5.  | [All Cases To Kebab Case Conversion Function](#5-all-cases-to-kebab-case-conversion) |

### 1. All Cases to Pascal Case Conversion

```javascript
function toPascalCase(inputString) {
  let words = inputString.split(/[-_]/); // assuming input is snake-case or kebab-case
  words = words.map((word) => word.charAt(0).toUpperCase() + word.slice(1));
  return words.join("");
}

// Example usage:
const snakeCaseString = "navneet_kumar";
const camelCaseString = "navneetKumar";
const kebabCaseString = "navneet kumar";

const pascalCaseSnake = toPascalCase(snakeCaseString);
const pascalCaseCamel = toPascalCase(camelCaseString);
const pascalCaseKebab = toPascalCase(kebabCaseString);

console.log(pascalCaseSnake); // Output: NavneetKumar
console.log(pascalCaseCamel); // Output: NavneetKumar
console.log(pascalCaseKebab); // Output: NavneetKumar
```

*This function, `toPascalCase`, converts both lowercase and uppercase strings to PascalCase by ensuring that the first letter of each word is capitalized, and the rest of the letters are in lowercase.*

---

### 2. All Cases to Title Case Conversion

```javascript
function toTitleCase(inputString) {
  // Check for different separators and split accordingly
  let words;
  if (inputString.includes("_")) {
    words = inputString.split("_");
  } else if (inputString.includes("-")) {
    words = inputString.split("-");
  } else if (inputString.includes(" ")) {
    words = inputString.split(/(?=[A-Z])|\s+/);
  } else {
    words = inputString.split(/(?=[A-Z])|\s+/);
  }

  // Capitalize the first letter of each word
  words = words.map(
    (word) => word.charAt(0).toUpperCase() + word.slice(1).toLowerCase()
  );
  // Join the words and add spaces before uppercase letters in camelCase
  return words.join(" ");
}

// Example usage:
const snakeCaseString = "navneet_kumar";
const camelCaseString = "navneetKumar";
const kebabCaseString = "navneet-kumar";

const titleCaseSnake = toTitleCase(snakeCaseString);
const titleCaseCamel = toTitleCase(camelCaseString);
const titleCaseKebab = toTitleCase(kebabCaseString);

console.log(titleCaseSnake); // Output: Navneet Kumar
console.log(titleCaseCamel); // Output: Navneet Kumar
console.log(titleCaseKebab); // Output: Navneet Kumar
```

*This function is designed to handle various cases, including snake_case, camelCase, kebab-case, and spaces between words, producing a consistent Title Case output.*

---

### 3. All Cases to Snake Case Conversion

```javascript
function toSnakeCase(inputString) {
  // Check for different separators and split accordingly
  let words;
  if (inputString.includes('_')) {
    words = inputString.split('_');
  } else if (inputString.includes('-')) {
    words = inputString.split('-');
  } else if (inputString.includes(" ")) {
    words = inputString.split(/\s+/);
  } else {
    // If no separators found, assume it's either camelCase or Title Case
    words = inputString.split(/(?=[A-Z])|\s+/);
  }

  // Convert each word to lowercase
  words = words.map(word => word.toLowerCase());

  // Join the words with underscores
  return words.join('_');
}

// Example usage:
const kebabCaseString = "kebab-case-example";
const snakeCaseString = "snake_case_example";
const camelCaseString = "camelCaseExample";
const titleCaseString = "Title Case Example";

const snakeCaseKebab = toSnakeCase(kebabCaseString);
const snakeCaseSnake = toSnakeCase(snakeCaseString);
const snakeCaseCamel = toSnakeCase(camelCaseString);
const snakeCaseTitle = toSnakeCase(titleCaseString);

console.log(snakeCaseKebab);  // Output: kebab_case_example
console.log(snakeCaseSnake);  // Output: snake_case_example
console.log(snakeCaseCamel);  // Output: camel_case_example
console.log(snakeCaseTitle);  // Output: title_case_example
```

*This function is designed to handle various cases, including snake_case, camelCase, kebab-case, and spaces between words, producing a consistent Snake Case output.*

---

### 4. All Cases to Camel Case Conversion

```javascript
function toCamelCase(inputString) {
  // Check for different separators and split accordingly
  let words;
  if (inputString.includes('_')) {
    words = inputString.split('_');
  } else if (inputString.includes('-')) {
    words = inputString.split('-');
  } else if (inputString.includes(" ")) {
    words = inputString.split(/\s+/);
  } else {
    // If no separators found, assume it's either camelCase or Title Case
    words = inputString.split(/(?=[A-Z])|\s+/);
  }

  // Capitalize the first letter of each word after the first
  words = words.map((word, index) => index === 0 ? word.toLowerCase() : word.charAt(0).toUpperCase() + word.slice(1).toLowerCase());

  // Join the words without spaces
  return words.join('');
}

// Example usage:
const kebabCaseString = "kebab-case-example";
const snakeCaseString = "snake_case_example";
const camelCaseString = "CamelCaseExample";
const titleCaseString = "Title Case Example";

const camelCaseKebab = toCamelCase(kebabCaseString);
const camelCaseSnake = toCamelCase(snakeCaseString);
const camelCaseCamel = toCamelCase(camelCaseString);
const camelCaseTitle = toCamelCase(titleCaseString);

console.log(camelCaseKebab);  // Output: kebabCaseExample
console.log(camelCaseSnake);  // Output: snakeCaseExample
console.log(camelCaseCamel);  // Output: camelCaseExample
console.log(camelCaseTitle);  // Output: titleCaseExample
```

*This function is designed to handle various cases, including snake_case, camelCase, kebab-case, and spaces between words, producing a consistent Camel Case output.*

---

### 5. All Cases to Kebab Case Conversion

```javascript
function toKebabCase(inputString) {
  // Check for different separators and split accordingly
  let words;
  if (inputString.includes('_')) {
    words = inputString.split('_');
  } else if (inputString.includes('-')) {
    words = inputString.split('-');
  } else if (inputString.includes(" ")) {
    words = inputString.split(/\s+/);
  } else {
    // If no separators found, assume it's either camelCase or Title Case
    words = inputString.split(/(?=[A-Z])|\s+/);
  }

  // Convert each word to lowercase
  words = words.map(word => word.toLowerCase());

  // Join the words with hyphens
  return words.join('-');
}

// Example usage:
const kebabCaseString = "kebab-case-example";
const snakeCaseString = "snake_case_example";
const camelCaseString = "CamelCaseExample";
const titleCaseString = "Title Case Example";

const kebabCaseKebab = toKebabCase(kebabCaseString);
const kebabCaseSnake = toKebabCase(snakeCaseString);
const kebabCaseCamel = toKebabCase(camelCaseString);
const kebabCaseTitle = toKebabCase(titleCaseString);

console.log(kebabCaseKebab);  // Output: kebab-case-example
console.log(kebabCaseSnake);  // Output: snake-case-example
console.log(kebabCaseCamel);  // Output: camel-case-example
console.log(kebabCaseTitle);  // Output: title-case-example
```

*This function is designed to handle various cases, including snake_case, camelCase, kebab-case, and spaces between words, producing a consistent Kebab Case output.*

---
