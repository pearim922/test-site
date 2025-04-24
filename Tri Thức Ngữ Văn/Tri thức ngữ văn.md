<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8">
  <title>Toggle Nội dung</title>
  <style>
    .toggle-container {
      margin: 20px;
      font-family: Arial, sans-serif;
    }

    .toggle-button {
      cursor: pointer;
      font-weight: bold;
      color: #2a6de6;
      background-color: #f0f0f0;
      padding: 10px;
      border-radius: 8px;
      transition: background-color 0.3s ease;
    }

    .toggle-button:hover {
      background-color: #dbe5ff;
    }

    .toggle-content {
      display: none;
      margin-top: 10px;
      padding: 10px;
      border-left: 3px solid #2a6de6;
      background-color: #f9f9f9;
      border-radius: 6px;
    }
  </style>
</head>
<body>
  <div class="toggle-container">
    <div class="toggle-button" onclick="toggleContent()">▶ Chỉ ra và nêu tác dụng của yếu tố phi ngôn ngữ</div>
    <div class="toggle-content" id="content">
      <p>- Yếu tố phi ngôn ngữ trong văn bản là: <strong>(hình ảnh, số liệu, câu in đậm)</strong>.</p>
      <p>- Tác dụng:</p>
      <ul>
        <li>Tăng sự thêm sinh động, hấp dẫn, sáng tỏ “thông tin”, giúp người đọc nắm bắt nhanh hơn.</li>
        <li>Trực quan hóa, cụ thể hóa các thông tin quan trọng.</li>
      </ul>
    </div>
  </div>

  <script>
    function toggleContent() {
      const content = document.getElementById("content");
      const button = document.querySelector(".toggle-button");
      const isVisible = content.style.display === "block";

      content.style.display = isVisible ? "none" : "block";
      button.innerHTML = isVisible 
        ? "▶ Chỉ ra và nêu tác dụng của yếu tố phi ngôn ngữ" 
        : "▼ Chỉ ra và nêu tác dụng của yếu tố phi ngôn ngữ";
    }
  </script>
</body>
</html>
