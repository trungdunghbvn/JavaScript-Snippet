# JavaScript-Snippet

Some of the JavaScript Snippets that are useful

## Mục lục

1. [All](#all)
2. [AllEqual](#all-equal)
3. [approximatelyEqual](#approximatelyEqual)
4. [arrayToCSV](#arrayToCSV)
5. [Lớp](#lớp)
6. [SOLID](#solid)
7. [Testing](#testing)
8. [Xử lí đồng thời](#xử-lí-đồng-thời)
9. [Xử lí lỗi](#xử-lí-lỗi)
10. [Định dạng](#Định-dạng)
11. [Viết chú thích](#viết-chú-thích)
12. [Các ngôn ngữ khác](#các-ngôn-ngữ-khác)

## **All**

### Kiểm tra các phần tử trong mảng có thỏa mãn điểu kiện đã cho không (fn). Khi không truyền tham số thứ 2, mặc định fn = true

```javascript
const all = (arr, fn = Boolean) => arr.every(fn);

all([4, 2, 3], (x) => x > 1); // true
all([1, 2, 3], (x) => x > 1); // false
all([1, 2, 3]); // true
```

**[⬆ về đầu trang](#mục-lục)**

## **All Equal**

### Kiểm tra các phần tử trong mảng có bằng nhau không

```javascript
const allEqual = (arr) => arr.every((val) => val === arr[0]);

allEqual([1, 2, 3, 4, 5, 6]); // false
allEqual([1, 1, 1, 1]); // true
```

**[⬆ về đầu trang](#mục-lục)**

## **approximatelyEqual**

### Kiểm tra hai số đã cho có xấp xỉ bằng nhau không với 1 sai số nhất định

```javascript
const approximatelyEqual = (n1, n2, epsilon = 0.001) => Math.abs(n1 - n2) < epsilon;

approximatelyEqual(Math.PI / 2.0, 1.5708); // true
approximatelyEqual(2, 1.5708); // false
approximatelyEqual(2, 1.5708, 1); // true
```

**[⬆ về đầu trang](#mục-lục)**
## **arrayToCSV**

### Convert các phần tử thành chuỗi với các giá trị được phân tách bằng dấu phẩy.

```javascript
const arrayToCSV = (arr, delimiter = ',') =>
  arr.map(val => val.map(item => `"${item}"`).join(delimiter)).join('\n');

arrayToCSV([['a', 'b'], ['c', 'd']]); // '"a","b"\n"c","d"'
arrayToCSV([['a', 'b'], ['c', 'd']], ':'); // '"a":"b"\n"c":"d"'
```

**[⬆ về đầu trang](#mục-lục)**
