# Introduction

Sự phát triển của công nghệ RGB-D và tương tác người - máy đã mở ra nhiều tiềm năng hỗ trợ người khiếm thị nhận biết môi trường, song các giải pháp hiện nay chủ yếu tập trung vào định hướng di chuyển diện rộng hoặc nghiên cứu riêng lẻ từng bài toán (nhận diện vật thể 3D, ước lượng tư thế bàn tay, phân loại kiểu cầm nắm) mà thiếu sự gắn kết thành một quy trình dẫn hướng khép kín. Nhằm giải quyết sự đứt gãy này, đề tài tập trung nghiên cứu giải pháp hỗ trợ người mù thực hiện thao tác cầm nắm trong “môi trường cảm thụ diện hẹp” – không gian cục bộ trong phạm vi với tay từ 0,3 đến 0,8 m – bằng cách tích hợp đồng bộ dữ liệu vị trí vật thể 3D, trạng thái bàn tay, quan hệ hình học tương đối và phản hồi tương tác (âm thanh/giọng nói) theo chu trình thống nhất: nhận diện đối tượng, xác định vị trí tương đối, hướng dẫn tiếp cận, gợi ý kiểu cầm và xác nhận thao tác thành công.

<figure>
  <img src="images/sơ đồ cấu trúc.jpg" alt="Mô tả ảnh" width="300" height="200"> 
  <figcaption>Hình 1: Minh họa tổng thể kiến trú</figcaption>
</figure>

