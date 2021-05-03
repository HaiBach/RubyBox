# RUBYBOX

## HƯỚNG DẪN SỬ DỤNG

1. Thêm thư viện `rubybox.js` và `rubybox.css` vào trang.
2. Markup trên trang
  Phải có đối tượng trỏ tới nơi hiển thị box
  ``` html
  <!-- Đối tượng đường link trỏ tới, thuộc tính `href`
  trỏ tới đối tượng trong rubybox -->
  <a class="rubybox" href="#"></a>

  <!-- Nội dung của rubybox, chứa trong div có `display: none;` -->
  <div style="display: none;">
    <div class="noidung">
      ...
    </div>
  </div>
  ```

3. Cài đặt javascript trên thể `<script>`
  ``` js
  $(document).on('ready', function() {
    var rubybox = $('.rubybox').rubybox({
      'width'       : 1280, // Kích thước của Rubybox
      'height'      : 1, // 100%, đơn vị là %
      'margin'      : [20, 10, 20, 10],
      'isOverClose' : false // Bấm vào vùng xunh quanh để tắt Rubybox
    });
  })
  ```