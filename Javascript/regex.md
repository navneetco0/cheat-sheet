# Regular Expressions in React

## 1. Decimal Numbers (Up to Two Decimal Places)

````javascript
const untillTwoDecimal = /^\d+(\.\d{0,2})?$|^\.(\d{1,2})?$|^$/;

This regular expression validates decimal numbers up to two decimal places.

## 2. Decimal Numbers with Metric Unit (Up to Three Decimals)

```javascript
const regexML = /^\d+(\.\d{0,3})?(m|ml)?$|^\.(\d{1,3})?(m|ml)?$|^$/;

This regular expression validates decimal numbers with an optional metric unit (m or ml) up to three decimal places.

## 3. Decimal Numbers with Weight Unit (Up to Three Decimals)

```javascript
const regexKG = /^\d+(\.\d{0,3})?(k|kg|g)?$|^\.(\d{1,3})?(k|kg|g)?$|^$/;

This regular expression validates decimal numbers with an optional weight unit (k, kg, or g) up to three decimal places.

## 4. Decimal Numbers (Up to Three Decimals)

```javascript
const untillThreeDecimal = /^\d+(\.\d{0,3})?$|^\.(\d{1,3})?$|^$/;

This regular expression validates decimal numbers up to three decimal places.

## 5. Percentage (Up to Two Decimals)

```javascript
const precentage = /^(100(\.0{1,2})?|[1-9]?\d(\.\d{1,2})?)$|^0(\.\d{1,2})?%$|^$/;

This regular expression validates percentages, allowing values from 0 to 100 with up to two decimal places.
