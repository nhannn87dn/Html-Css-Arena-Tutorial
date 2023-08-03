# CSS3-Animation


## 2.1 Transition


Transition hoạt động bằng cách thay đổi giá trị thuộc tính một cách trơn tru từ giá trị NÀY sang giá trị KHÁC trong khoảng thời gian nhất định. Các tham số thường được sử dụng:

- transition-delay: khoảng thời gian dừng cho mỗi hiệu ứng chuyển đổi.
- transition-duration: khoảng thời gian chuyển đổi diễn ra.
- transition-property: thuộc tính cần chuyển đổi.
- transition-timing-function: tốc độ chuyển đổi diễn ra

Cú pháp: 

```css
div {
  width: 100px;
  height: 100px;
  background: red;

  transition-property: width;
  transition-duration: 2s;
  transition-timing-function: linear;
  transition-delay: 1s;
  /* shorthand */
  transition: width 2s linear 1s;
}
/* rê chuột lên thẻ div sẽ thay đổi chiều rộng lên 300px */
div:hover {
  width: 300px;
}
```

Thuộc tính transition-timing-function dùng để xác định tốc độ thay đổi khi chuyển đổi.

Các giá trị có sẵn như sau:

- ease: tạo hiệu ứng chuyển đổi khi bắt đầu thì chậm sau đó nhanh dần và gần kết thúc lại chậm từ từ (giá trị mặc định).
- linear: tạo hiệu ứng chuyển đổi từ lúc bắt đầu với lúc kết thúc tốc độ là như nhau.
- ease-in: tạo hiệu ứng chuyển đổi chậm ở lúc bắt đầu.
- ease-out: tạo hiệu ứng chuyển đổi chậm ở lúc kết thúc.
- ease-in-out: tạo hiệu ứng chuyển đổi chậm ở lúc bắt đầu và lúc kết thúc.


 Demo transition-timing-function: 
<https://www.joshwcomeau.com/animation/css-transitions/>


## 2.2 Animation - hoạt cảnh

-  **@keyframes**: dùng để thiết lập một chuyển động

    Cú Pháp 

    ```css
    @keyframes nameAnimation {
        ...code
    }
    ```

    Trong đó

    nameAnimation: là tên của chuyển động.

    Code: là các đoạn code cho tiến trình chuyển động.

- **animation-name**:  tác dụng xác định thành phần sẽ thực thi animation nào
    
    Cú pháp:
    ```css
    animation-name: nameAnimation;
    ```
- **animation-duration**: thiết lập khoảng thời gian thực thị 1 chuyển động animation

    Cú pháp: 
    ```css
    animation-duration: 2s; /* time - seconds */
    ```

- **animation-timing-function** : xác định tốc độ chuyển động của một animation sẽ như thế nào
    Cú pháp: 
    ```css
    animation-timing-function: value; /* ease, linear...*/
    ```
- animation-delay : xác định độ trễ của mỗi lượt chuyển động
    Cú pháp: 
    ```css
    animation-delay: 2s; /* time - seconds */
    ```
- **animation-iteration-count**: thiết lập số lần thực hiện một animation
    Cú pháp: 
    ```css
    animation-iteration-count: number | infinite;
    ```
    Với `infinite` là lặp vô tận
- **animation-direction** : xác định xem chiều chạy của animation sẽ như thế nào
    Cú pháp: 
    ```css
    aniamtion-direction: normal|reverse|alternate|alternate-reverse|initial|inherit;
    ```
- **animation-fill-mode**: xác định trạng thái của một animation, khi mà animation không được chạy (có thể là animation này đã chạy xong hoặc đang bị delay)
    Cú pháp: 
    ```css
    animation-fill-mode: none|forwards|backwards|both|initial|inherit;
    ```
- **animation-play-state**: xác định trạng thái của animation
    Cú pháp: 
    ```css
    animation-duration: paused|running|initial|inherit;
    ```

Các bạn có thể search keywords: Ví dụ: animation-fill-mode w3school --> để xem ví dụ từng trường hợp.

Ví dụ giải thích từng thuộc tính: <https://viblo.asia/p/hieu-biet-them-ve-animation-trong-css3-gDVK2wOeZLj>

Demo cách áp dụng: <https://quantrimang.com/hoc/animation-trong-css-163546>

====================================

## 2.3 Transforms 2D, 3D - biến hình, thay đổi hình dạng

Xem thêm: 
- <https://www.w3schools.com/css/css3_2dtransforms.asp>
- <https://www.w3schools.com/css/css3_3dtransforms.asp>

==============

Xem thêm tài liệu: 

- <https://animate.style/#best-practices>
- <https://www.w3schools.com/css/css3_animations.asp>
- <https://www.w3schools.com/cssref/css_animatable.php>
- <https://michalsnik.github.io/aos/>

Một số Demo: <https://blog.hubspot.com/website/css-animation-examples>


