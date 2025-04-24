<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Toggle Thể Thơ</title>
  <style>
    .toggle {
      border: 1px solid #ccc;
      border-radius: 8px;
      padding: 10px;
      margin: 10px 0;
    }
    .toggle-title {
      font-weight: bold;
      cursor: pointer;
      padding: 5px;
      background-color: #f0f0f0;
      border-radius: 6px;
    }
    .toggle-content {
      display: none;
      margin-top: 5px;
      padding-left: 10px;
    }
  </style>
</head>
<body>

<div class="toggle">
  <div class="toggle-title" onclick="toggleContent(this)">Chỉ ra thể thơ và dấu hiệu nhận biết của nó</div>
  <div class="toggle-content">

    <div class="toggle">
      <div class="toggle-title" onclick="toggleContent(this)">Chú ý</div>
      <div class="toggle-content">
        Đếm xem mỗi dòng có bao từ rồi ghi ra cuối câu, đừng đếm có 1-2 dòng đầu hay dòng cuối.
      </div>
    </div>

    <div class="toggle">
      <div class="toggle-title" onclick="toggleContent(this)">Trình bày</div>
      <div class="toggle-content">
        <strong>Tự do</strong>: Số chữ giữa mỗi câu khác nhau.<br>
        <strong>Lục bát</strong>: Các câu có 6 và 8 chữ xen kẽ nhau.<br>
        <strong>Thơ 4,5,6,7,8 chữ</strong>: Hoàn cảnh sáng tác thời cổ thì nói phiên âm (ngũ,tứ,bát,…ngôn). Còn viết thời hiện đại, ngôn từ mới thì nói bình thường (5,6,7,…chữ).<br>
        <strong>Song thất lục bát</strong>: 2 câu đầu 7 chữ, các câu còn lại 6 và 8 chữ xen kẽ nhau.<br>
        <strong>Thất ngôn tứ tuyệt</strong>: cả bài có 4 câu, mỗi câu 7 chữ.
      </div>
    </div>

  </div>
</div>

<script>
  function toggleContent(element) {
    const content = element.nextElementSibling;
    if (content.style.display === "block") {
      content.style.display = "none";
    } else {
      content.style.display = "block";
    }
  }
</script>

</body>
</html>
