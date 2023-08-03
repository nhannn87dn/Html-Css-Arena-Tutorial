
# CSS3 on Mobile devices (Responsive)

**Responsive** là gì ? Là kiểu hiển thị thích ứng, để làm sao khi xem trên các kích thước trình duyệt có màn hình hiển thị khác nhau như Desktop, Tablet, Mobile thì nó đều hiển thị cân đối, đầy đủ, thân thiện người dùng.

### 4.1 Viewport

Viewport là khung hình người dùng nhìn thấy trên thiết bị của họ khi vào một trang web bất kì. Với mỗi thiết khác nhau lại có viewport khác nhau.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">

```

`width=device-width`: thiết lập chiều rộng của trang web theo chiều rộng của thiết bị

`initial-scale=1.0`: thiết lập mức độ zoom ban đầu khi trang web được load bởi trình duyệt

### 4.2 Media Queries

>Media Queries là một kỹ thuật CSS được giới thiệu trong CSS3. Ta sử dụng cú pháp @media để bao gồm một khối các thuộc tính CSS chỉ khi một điều kiện nhất định là đúng. Nói một cách đơn giản là ta sẽ định nghĩa CSS riêng cho một nhóm các thiết bị có kích thước giống nhau.

**Media Queries là cốt lõi để xây dựng một website có Responsive**

Cú pháp:

```css
@media not|only media_type and (feature:value) {
  CSS-Code;
}
```

Trong đó `media_type` có các giá trị:
| Giá trị | Mô tả|
|---------|------|
| all     | Tất cả thiết bị |
| screen | Màn hình desktop, tablet, mobile |
| print | khi in ấn |

Còn `feature:value` là biểu thức điều kiện

feature thường dùng nhất: min-width, max-width, device-min-width, device-max-width

Ví dụ Media theo quy tắc Mobile First

```css
*{
    margin: 0
}

body{
    font-family: Roboto;
    line-height: 1.4
}

/*Smart phone nhỏ*/
@media screen and (min-width: 320px){
    /*Áp dụng cho kích thước trình duyệt có chiều rộng tối thiểu >= 320px*/
    h1{
        color: red;
        font-size: 20px
    }
}
/*Iphone (480 x 640)*/
@media screen and (min-width: 375px){
     h1{
        font-size: 30px
    }
    /* h1 sẽ thừa kế được thuộc tính color từ điều kiện trước, và chỉ thay đổi font-size */
}
/*Tablet nhỏ (480 x 640)*/
@media screen and (min-width: 480px){

}
/*Ipad dọc (768 x 1024)*/
@media screen and (min-width: 768px){

}
/*Ipad ngang(1024 x 768)*/
@media screen and (min-width: 1024px){

}
/*Desktop (1200 x 768)*/
@media screen and (min-width: 1200px){

}

```
![mobile first](mobile-first.webp)


Ví dụ Media theo quy tắc Desktop First


Theo mình cứ nhớ công thức là max-width = min-width – 1 vậy đúng sẽ là max-width: 1023px nhé các bạn

```css

*{
    margin: 0
}

body{
    font-family: Roboto;
    line-height: 1.4
}

/*Desktop (1200 x 768)*/
@media screen and (max-width: 1199px){
    /*Áp dụng cho kích thước trình duyệt có chiều rộng tối đa <= 1200px */
}

/*Ipad ngang(1024 x 768)*/
@media screen and (max-width: 1023px){

}

/*Ipad dọc(768 x 1024)*/
@media screen and (max-width: 767px){

}
/*Tablet nhỏ(480 x 640)*/
@media screen and (max-width: 479px){

}
/*Iphone(480 x 640)*/
@media screen and (max-width: 374px){

}
/*Smart phone nhỏ*/
@media screen and (max-width: 319px){

}

```

Lưu ý: Phần CSS nằm ngoài @media là dùng chung.

>Tìm hiểu thêm: Nên theo trường phái nào ? Mobile First hay Desktop First ?

- <https://www.w3schools.com/css/css3_mediaqueries.asp>
- <https://www.w3schools.com/css/css3_mediaqueries_ex.asp>

