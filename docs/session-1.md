# Buổi 1: Giới thiệu cơ bản về CSS.

## Css syntax

Dưới đây là 1 đoạn code css.

```
div.box {
    color: rgb(170, 0, 210) !important;
}

div.main > table {
    border-collapse: collapse;
    border: thin green solid;
    width: 60%;
}
```
  Nếu bạn là 1 người chưa biết về css thì nhìn đoạn code trên có vẻ khó hiểu.
  Nhưng tôi sẽ cố gắng trình bày 1 cách cặn kẽ để bạn có thể hiểu được vì sao css được viết như trên.

Ok, ta có 1 ví dụ như sau:
```
h1 {
    color: red;
    font-size: 16px;
}
```

Ta phát biểu như sau:
- h1 -> selector
- color -> property
- red -> value

Bổ sung thêm:
- Attribute
- Attribute name (property)
- Attribute value (value)

Nhìn cú pháp trên giống object trong JavaScript.
```
const myStyle = {
    color: 'red',
    'font-size': '16px'
};
```
Trong object js ta gọi nó là **key-value**. 
Tuy nhiên trong css ta nó với thuật ngữ là **attribue**.

## DOM (Document Object Model) Tree?
Trước khi tìm hiểu CSS chúng ta nên hiểu về DOM tree.
- Hiểu đơn giản DOM Tree (Cây mô hình đối tượng tài liêụ) là 1 cấu trúc dữ liệu phân cấp mà trình duyệt (browser) dùng nó để biểu diễn cấu trúc của 1 trang web hoặc 1 tài liệu HTML/XML.
<br/>
<br/>

Dưới đây là 1 ví dụ về DOM tree.



<p align="center">
  <img src="./images/dom-tree.gif"  width="600" height="400">
</p>
<br/>

Hình ảnh trên mô tả đoạn code **HTML** dươí đây
```
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>My title</title>
</head>
<body>
    <a href="https://google.com">My link</a>
    <h1>My header</h1>
</body>
</html>
```
<br>

## CSS selector
Trong phần này ta sẽ học cách sử dụng các **selector** đơn giản nhất để css được *element* nào đấy trong document của mình.
<br/>
Trong phần này tôi sẽ demo 4 cách dùng selector cơ bản trong CSS.
<br/>
### 4 cách dùng selector cơ bản:
- **selector với tag name** <br />
Tức là ta có thể dùng các tên thẻ làm selector.
Các thẻ như: **div, session, p, a, nav...** <br/>
Ví dụ: tôi muốn tạo ra 1 đoạn văn bản có chữ màu đỏ.
```
  p {
    color: red;
  }
```
- **Select element by id** <br/>
Trong 1 document có thẻ mà có attribute là id thì ta có thể dựa vào id để select element đó. <br/>
Ví dụ: Trong document **có id là table-staff-list** và tôi muốn tăng chiều rộng là 600px.

```
<!-- Đây là code HTML -->
<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <title>My title</title>
</head>
<body>
    <a href="https://google.com">My link</a>
    <h1>My header</h1>
    <div id="table-staff-list">xxx</div>
    <div class="item">yyy</div>
</body>
</html>

<!-- Đây là code css -->
table-staff-list {
  width: 600px;
}
```

- **Select element by class name** <br/>
Giống như select theo id thì ta có class. <br/>
Ví dụ: Dựa vào đoạn HTML bên trên ta sẽ css cho **class là item** có cỡ chữ là 16px và cẵn giữa.

```
  .item {
    font-size: 16px;
    text-align: center;
  }
```

- **Select a group** <br/>
Tức là ta có thể css 1 lúc nhiều elements.
Dưới đây là 1 ví dụ về css vừa thẻ p, vừa class item có chữ màu xanh dương.
```
  p, .item {
    color: blue;
  }
```
<br/>

## Colors in CSS
Trong CSS có 3 cách dùng màu chính.
- RGB Hex (#00FF00) <br>
Trong đó:
  - 2 kí tự 00 đầu là tượng trưng cho màu đỏ.
  - 2 kí tự FF giữa tượng trưng cho màu xanh lá.
  - 2 kí tự 00 cuối bên phải tượng trưng cho màu xanh dương.
  - Gồm 16 kí tự (HEX): 1 2 3 4 5 6 7 8 9 10 A B C D E F -> 1 càng về phía F thì sẽ nhạt hơn, trắng dần.
  - VD: màu đỏ -> #FF0000 
- rgb(red, green, blue)
  - red, green, blue có giá trị là số nguyên.
  - từ 0 tới 255
  - VD: Màu xanh lá: rgb(00, 255, 00)
- rgba(red, green, blue, alpha) <br>
Tương tự như rgb tuy nhiên có 1 tham số là alpha.
  - alpha là tham số dùng để tăng giảm độ trong suốt. Có value là số thực.
  - Từ 0 -> 1
  - VD: màu đỏ nhưng chỉ hiển thị 50% -> rgba(255, 0, 0, 0.5) hoặc rgba(255, 0, 0, .5)
<br/>

## Styling text
Ở phần này chúng ta cùng tìm hiểu các attribue để style cho text trong document nhé.

| property  | value
| -------   | ---- |
| color    | Hex code or rgb() or rgab()   |
| text-align    | center \| left \| right \| justify   |
| text-decoration    | none \| underline \| overline \| line-through   |
| text-indent    |  Xpx  |
| letter-spacing    |  Xpx  |
| word-spacing    |  Xpx  |
| line-heigh |  là 1 số \| ví dụ: 1.5  |
| text-shadow    |  x y color blur  |


## Chia sẻ cách nhớ các attributes trong CSS
1. Khi gần laptop -> không có gì ngoài cách gõ nhiều, hiểu lệnh mình viết ra.
2. Khi không gần laptop -> ghi chú ra 1 quyển sổ tay, giấy nhớ...