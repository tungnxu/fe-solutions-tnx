# Standard Base CSS

## Vấn đề
Các trình duyệt có bộ render khác nhau, các quy chuẩn render khác nhau nên UI Web khi được render ra có thể hiển thị khác nhau 1 chút giữa các trình duyệt. Bởi vậy, để tạo UI được đảm bảo độ chính xác nhất như bản Design, ở trên đa số trình duyệt, chúng tá sẽ  cần reset CSS để đảm bảo tính thống nhất về UI giữa các trình duyệt.  

## Giải pháp
* Sử dụng các CSS Framework phổ biến (bootstrap ..v.v.) (Họ đã )
* Sử dụng Reset/Frameworks như **css reset** hoặc **Normalize.CSS** . 

## Kinh nghiệm

```css
/* 
Thuộc tính đảm bảo box-sizing luôn là border-box toàn size
*/
*, ::before, ::after { box-sizing: border-box; }


/**
Thống nhất line height toàn bộ trình duyệt
Chống sai lệch cỡ chữ trên ios
 */
html {
  line-height: 1.15; /* 1 */
  -webkit-text-size-adjust: 100%; /* 2 */
}

/**
Xóa bỏ margin trên mọi trình duyệt
Thiết lập các thông số cơ bản Fontsize , kiểu font, màu chữ, màu nền, font weight..
Font-smoothing làm mượt chữ trên trình duyệt safari, đảm bảo kiểu chữ tương đồng 

 */
body {
  margin: 0;

  font-family: 'Chillax', sans-serif;
  font-size: 16px;
  color: #ffffff;
  background-color: #041133;
  font-weight: normal;

  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

small {
  font-size: 80%;
}

button,
[type='button'],
[type='reset'],
[type='submit'] {
  -webkit-appearance: button;
}

/* 
Các element HTML5 mặc định kiểu block
*/
article, aside, details, figcaption, figure, footer, header, hgroup, main, nav, section {
  display: block;
}



/* 
Header size quy chuẩn với 1rem = 16px, (nếu cần)
H1: 2rem = 32px
H2: 1.5rem = 24px
H3: 1.125rem = 18px 
H4: 1rem = 16px 
*/
h1 { font-size: 2rem; }
h2 { font-size: 1.5rem; }
h3 { font-size: 1.125rem; }
h4 { font-size: 1.00rem; }
h5 { font-size: 0.83rem; }
h6 { font-size: 0.67rem; }

/* 
Nếu bạn sử dụng Hr
*/
hr {
  border-style: solid;
  border-width: 1px 0 0;
  color: inherit;
  height: 0;
  overflow: visible;
}

```

## Reference
[css-remedy](https://css-tricks.com/css-remedy/)