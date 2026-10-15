# 1. Quy trình thu thập dữ liệu

## 1.1. Thiết bị thu thập dữ liệu

Nghiên cứu sử dụng camera đo chiều sâu Intel RealSense D435, tích hợp hai cảm biến hồng ngoại, máy chiếu điểm hồng ngoại và camera RGB, cho phép thu thập đồng thời dữ liệu chiều sâu và hình ảnh màu của môi trường. Camera được kết nối với máy tính qua USB 3.0 và sử dụng phần mềm Intel RealSense Viewer để cấu hình, ghi dữ liệu vào tệp định dạng `.bag`.

<p align="center">
<div style="display: flex; gap: 10px;">
  <img src="Images/camera.jpg" width="100%">
</div>

*Hình 1. Camera Intel RealSense D435 sử dụng trong hệ thống thu thập dữ liệu.*

Để ghi lại hình ảnh theo góc nhìn thứ nhất (First-Person View – FPV), hệ thống sử dụng laptop MSI B12MO với bộ xử lý Intel Core i5-1235U, RAM 16 GB và đồ họa tích hợp Intel Iris Xe. Video được ghi ở độ phân giải 640 × 480 pixel, tốc độ 30 khung hình/giây (FPS).

## 1.2. Bối cảnh và bố trí không gian thực nghiệm

Thí nghiệm được thực hiện trong phòng ăn có diện tích khoảng 15 m², với các chướng ngại vật gồm bàn, ghế và chậu hoa nhằm mô phỏng môi trường sinh hoạt trong nhà. Các marker kích thước 10 × 10 cm được bố trí trên sàn để xác định tuyến đường và thứ tự di chuyển của người tham gia.

<p align="center">
<div style="display: flex; gap: 10px;">
  <img src="Images/so_do.jpg" width="100%">
</div>

*Hình 2. Sơ đồ bố trí không gian thực nghiệm, vị trí chướng ngại vật và tuyến đường di chuyển theo các marker.*

## 1.3. Bố trí hệ thống ghi hình

Camera được cố định trước ngực người tham gia, hướng về phía trước để ghi nhận môi trường theo hướng di chuyển. Laptop được đeo phía sau lưng nhằm hỗ trợ ghi và lưu trữ dữ liệu trong suốt quá trình thực nghiệm. Trước mỗi lần ghi hình, hệ thống được kiểm tra để bảo đảm thiết bị hoạt động ổn định.

<p align="center">
<div style="display: flex; gap: 10px;">
  <img src="Images/bo_tri.jpg" width="100%">
</div>

*Hình 3. Bố trí thiết bị ghi hình trên người tham gia: (a) tư thế đeo và hướng camera; (b) vị trí laptop phía sau lưng; (c) vị trí bắt đầu thu thập dữ liệu.*

## 1.4. Quy trình di chuyển và tổ chức dữ liệu

Người tham gia di chuyển theo tuyến đường đã xác định, bắt đầu tại marker số 25, đi qua các marker trung gian và kết thúc tại marker số 24. Mỗi video gồm bốn lượt di chuyển liên tiếp:

1. **Lượt đi 1:** từ marker 25 đến marker 24.
2. **Lượt về 1:** từ marker 24 trở lại marker 25.
3. **Lượt đi 2:** từ marker 25 đến marker 24.
4. **Lượt về 2:** từ marker 24 trở lại marker 25.

Quy trình này giúp thu thập dữ liệu theo cả hai hướng di chuyển và tăng tính nhất quán trong quá trình khảo sát môi trường. Thí nghiệm được thực hiện với năm tình nguyện viên, tương ứng năm video. Sau khi ghi hình, dữ liệu được thống kê theo từng video và từng lượt đi, lượt về để kiểm tra số lượng khung hình. Tổng cộng, bộ dữ liệu thu thập được gồm **46.072 khung hình**, phục vụ các bước xử lý và nghiên cứu tiếp theo.

**Bảng 1. Thống kê số lượng khung hình theo từng lượt di chuyển của 5 video**

<table>
  <thead>
    <tr>
      <th align="center">Video</th>
      <th align="center">Lượt</th>
      <th align="center">Số frame</th>
      <th align="center">Video</th>
      <th align="center">Lượt</th>
      <th align="center">Số frame</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td align="center" rowspan="4">1</td>
      <td align="center">Đi 1</td>
      <td align="center">3403</td>
      <td align="center" rowspan="4">4</td>
      <td align="center">Đi 1</td>
      <td align="center">1604</td>
    </tr>
    <tr>
      <td align="center">Về 1</td>
      <td align="center">3165</td>
      <td align="center">Về 1</td>
      <td align="center">1775</td>
    </tr>
    <tr>
      <td align="center">Đi 2</td>
      <td align="center">2593</td>
      <td align="center">Đi 2</td>
      <td align="center">1570</td>
    </tr>
    <tr>
      <td align="center">Về 2</td>
      <td align="center">2359</td>
      <td align="center">Về 2</td>
      <td align="center">1336</td>
    </tr>
    <tr>
      <td align="center" rowspan="4">2</td>
      <td align="center">Đi 1</td>
      <td align="center">2296</td>
      <td align="center" rowspan="4">5</td>
      <td align="center">Đi 1</td>
      <td align="center">3199</td>
    </tr>
    <tr>
      <td align="center">Về 1</td>
      <td align="center">2001</td>
      <td align="center">Về 1</td>
      <td align="center">3149</td>
    </tr>
    <tr>
      <td align="center">Đi 2</td>
      <td align="center">2026</td>
      <td align="center">Đi 2</td>
      <td align="center">2620</td>
    </tr>
    <tr>
      <td align="center">Về 2</td>
      <td align="center">1777</td>
      <td align="center">Về 2</td>
      <td align="center">2177</td>
    </tr>
    <tr>
      <td align="center" rowspan="4">3</td>
      <td align="center">Đi 1</td>
      <td align="center">3052</td>
      <td colspan="3"></td>
    </tr>
    <tr>
      <td align="center">Về 1</td>
      <td align="center">2065</td>
      <td colspan="3"></td>
    </tr>
    <tr>
      <td align="center">Đi 2</td>
      <td align="center">2099</td>
      <td colspan="3"></td>
    </tr>
    <tr>
      <td align="center">Về 2</td>
      <td align="center">1806</td>
      <td colspan="3"></td>
    </tr>
  </tbody>
</table>

*Bảng 1. Thống kê số lượng khung hình theo lượt đi và lượt về của năm video thu thập.*



