# MÔN HỌC: PHÁT TRIỂN ỨNG DỤNG TRÊN THIẾT BỊ DI ĐỘNG - TEE0419
---
# PHẦN 1: MIT APP INVENTOR (Quy trình tạo phần mềm)
<img width="1917" height="1025" alt="image" src="https://github.com/user-attachments/assets/9ca2604d-4b4d-4c3c-8e6f-06d616dbace4" />

## 1. Khái quát giao diện (Thanh công cụ, Kéo thả & Thuộc tính)

### Thanh công cụ (Palette)

Là kho chứa các "nguyên liệu" (Components) như Button, Label, TextBox, WebViewer,...

### Kéo thả (Drag & Drop)

Chỉ cần chọn component bên Palette và kéo thả vào màn hình điện thoại ảo (Viewer). Việc này giúp thiết kế giao diện trực quan (WYSIWYG - Thấy gì được nấy) mà không cần code.

### Thay đổi thuộc tính (Properties)

Khi click vào một component, cột Properties bên phải sẽ hiện ra. Dùng nó để chỉnh màu sắc, kích thước chữ, nội dung text, hình nền,... để "trang điểm" cho các đối tượng.

---

## 2. Bản chất của Blocks & Backpack

### Bản chất

Thay vì gõ từng dòng lệnh phức tạp, MIT App Inventor cho phép lắp ráp các khối lệnh (Blocks) giống như chơi Lego. Mỗi khối đại diện cho một hàm, vòng lặp, hoặc sự kiện.

### Ưu điểm

- Không bao giờ bị lỗi cú pháp (thiếu dấu phẩy, dấu chấm phẩy).
- Tư duy logic vô cùng trực quan.
- Cực kỳ thân thiện để phát triển nhanh (RAD).

### Nhược điểm

- Màn hình code dễ bị rối rắm (spaghetti blocks) khi app lớn.
- Khó áp dụng các thuật toán quá phức tạp.
- Khó quản lý mã nguồn nhóm (version control).

### Backpack (Cái balo)

Biểu tượng balo góc phải trên cùng. Có thể kéo các cụm Blocks thả vào balo để "copy", sau đó mở một Screen khác hoặc Project khác, mở balo ra và lôi cụm Blocks đó vào để "paste".

Cực kỳ tiện lợi để tái sử dụng code.

---
## 3. Hướng dẫn làm App 3 Screens

Đăng nhập vào MIT App Inventor và tạo một Project mới (ví dụ tên là `BaiTapLon_TEE0419`).
<img width="1917" height="1023" alt="Screenshot 2026-06-08 211006" src="https://github.com/user-attachments/assets/af259505-8a0e-42ca-a8b9-18e45fdfc0c1" />

Giao diện MIT App Inventor chia làm 2 chế độ chính ở góc phải trên cùng:
<img width="363" height="140" alt="Screenshot 2026-06-08 212357" src="https://github.com/user-attachments/assets/f0bc8962-6f4f-446d-8537-b653b7868ed0" />

- **Designer (Thiết kế):** Nơi kéo thả giao diện.
- **Blocks (Lập trình):** Nơi lắp ráp các khối logic.

Dưới đây là chi tiết từng bước xây dựng 3 Screens:

---

# BƯỚC 1: XÂY DỰNG SCREEN 1 (Màn hình About)
<img width="1919" height="1021" alt="Screenshot 2026-06-08 211028" src="https://github.com/user-attachments/assets/8371d0d4-2707-4519-ab1a-a8ddd8024a52" />

Đây là màn hình khởi chạy đầu tiên của ứng dụng. Nhiệm vụ của nó là hiển thị thông tin và điều hướng.

## 1. Phần Designer (Thiết kế giao diện)

### Bước 1.1

Nhìn sang cột Palette (bên trái), mục User Interface, kéo thả một Label vào màn hình điện thoại (Viewer).

### Bước 1.2

Click vào Label vừa kéo.

Nhìn sang cột Properties (bên phải), tìm thuộc tính Text và đổi thành thông tin cá nhân.

Ví dụ:

```text
Ứng dụng được phát triển bởi Hầu Nhật Ninh
```

Có thể chỉnh thêm FontSize cho to rõ.

### Bước 1.3

Kéo thả tiếp một Button vào màn hình.

Đổi tên quản lý của nút này (nút Rename ở cột Components) thành:

```text
btnToan
```

Chỉnh thuộc tính Text của nó thành:

```text
Giải Toán
```

### Bước 1.4

Kéo thả thêm một Button thứ hai.

Đổi tên thành:

```text
btnWeb
```

Chỉnh thuộc tính Text thành:

```text
Xem Web
```
<img width="1918" height="1020" alt="Screenshot 2026-06-08 212332" src="https://github.com/user-attachments/assets/e8b14549-4eb1-4d93-b83c-320728cccaac" />

---

## 2. Phần Blocks (Lập trình logic)

### Bước 2.1

Chuyển sang chế độ Blocks (Góc phải trên cùng).
<img width="1919" height="1027" alt="Screenshot 2026-06-08 212409" src="https://github.com/user-attachments/assets/77b4493b-789b-4ade-9cba-bd1c22f5ca6d" />

### Bước 2.2

Cột bên trái, click vào `btnToan`.
<img width="723" height="790" alt="Screenshot 2026-06-08 213448" src="https://github.com/user-attachments/assets/fb9e1d5b-dcd0-4a75-95e5-16c652b37c8f" />

Chọn khối vàng có chữ:

```text
when btnToan.Click do
```

và kéo ra màn hình trắng.

### Bước 2.3

Click vào mục Control (màu vàng nhạt), kéo khối:

```text
open another screen screenName
```

ghép vào rãnh trống của khối:

```text
when btnToan.Click do
```
<img width="767" height="514" alt="Screenshot 2026-06-08 213523" src="https://github.com/user-attachments/assets/09649ef2-59db-4732-b2ed-bfa0a41884ec" />

### Bước 2.4

Click vào mục Text (màu hồng), kéo khối có dấu ngoặc kép:

```text
" "
```

ghép vào đuôi của khối:

```text
open another screen
```
<img width="590" height="476" alt="Screenshot 2026-06-08 213712" src="https://github.com/user-attachments/assets/1791e220-4096-4967-94ff-350deabea142" />

Gõ:

```text
Screen2
```

vào bên trong dấu ngoặc kép.

> Lưu ý: Gõ chính xác chữ hoa và chữ thường.
<img width="464" height="119" alt="Screenshot 2026-06-08 213856" src="https://github.com/user-attachments/assets/2c4b64c9-485b-42a0-893b-05b3ab7800a0" />

### Bước 2.5

Làm lặp lại từ Bước 2.2 đến 2.4 cho nút `btnWeb`, nhưng thay chữ trong ngoặc kép thành:

```text
Screen3
```
<img width="1919" height="1023" alt="Screenshot 2026-06-08 213955" src="https://github.com/user-attachments/assets/f05fd460-2ff4-4830-8d0c-6aa8dcb79802" />

---

# BƯỚC 2: XÂY DỰNG SCREEN 2 (Màn hình Giải toán)

Tạo Screen mới:

Ở thanh menu trên cùng, bấm nút:

```text
Add Screen
```

Nhập tên:

```text
Screen2
```

(Không chứa khoảng trắng) rồi bấm OK.
<img width="1919" height="1028" alt="Screenshot 2026-06-08 214137" src="https://github.com/user-attachments/assets/97c4989f-a5a0-4778-9e7f-5e8cfa646d39" />

---

## 1. Phần Designer (Thiết kế giao diện)

### Bước 1.1

Kéo thả một TextBox (ô nhập liệu).

Đổi tên nó thành:

```text
txtA
```
<img width="619" height="460" alt="Screenshot 2026-06-08 214308" src="https://github.com/user-attachments/assets/89724da7-2d38-4c91-a5a5-4a0d95199c41" />

Trong cột Properties, tìm thuộc tính Hint và gõ:

```text
Nhập số A
```
<img width="377" height="193" alt="Screenshot 2026-06-08 214404" src="https://github.com/user-attachments/assets/5b2782ac-d2d8-402b-a8cb-af757b1d0096" />

Tích chọn ô:

```text
NumbersOnly
```

để bàn phím chỉ hiện số.
<img width="319" height="284" alt="Screenshot 2026-06-08 214420" src="https://github.com/user-attachments/assets/f180b60d-f77e-43a5-b0df-1fdc70f8bbb8" />

### Bước 1.2

Kéo thả một TextBox thứ hai.

Đổi tên thành:

```text
txtB
```
<img width="584" height="365" alt="Screenshot 2026-06-08 214451" src="https://github.com/user-attachments/assets/449e86a0-cf5d-42ed-8e89-b7e8f79a912c" />

Hint:

```text
Nhập số B
```

và cũng chọn:

```text
NumbersOnly
```

### Bước 1.3

Kéo thả một Button.

Đổi tên thành:

```text
btnTinh
```
<img width="651" height="334" alt="Screenshot 2026-06-08 214535" src="https://github.com/user-attachments/assets/8b9ef054-2ae8-49e1-8928-b1d62cfb370f" />

Đổi Text thành:

```text
Tính Tổng
```

### Bước 1.4

Kéo thả một Label.

Đổi tên thành:

```text
lblKetQua
```
<img width="715" height="332" alt="Screenshot 2026-06-08 214616" src="https://github.com/user-attachments/assets/d0a44c09-0f9a-4315-9e39-bae1aff7c903" />

Đổi Text thành:

```text
Kết quả:
```

Chỉnh màu chữ (TextColor) sang màu đỏ cho nổi bật.
<img width="590" height="357" alt="Screenshot 2026-06-08 214706" src="https://github.com/user-attachments/assets/129963e8-daad-4083-89d1-add6488d682f" />

---

## 2. Phần Blocks (Lập trình logic)

### Bước 2.1

Chuyển sang Blocks.

Click `btnTinh`, kéo khối sự kiện:

```text
when btnTinh.Click do
```

ra màn hình.
<img width="642" height="661" alt="Screenshot 2026-06-08 214741" src="https://github.com/user-attachments/assets/11f6f5f8-226e-4e23-a4ae-059f43f5cdcd" />

### Bước 2.2

Click `lblKetQua`, cuộn xuống tìm và kéo khối:

```text
set lblKetQua.Text to
```

ghép vào bên trong.
<img width="651" height="742" alt="Screenshot 2026-06-08 214817" src="https://github.com/user-attachments/assets/e612913b-a6d8-4232-b179-cb5e6a02c70c" />

### Bước 2.3

Click vào mục Math (màu xanh dương), tìm khối phép cộng:

```text
+
```

và ghép vào đuôi khối ở trên.

Khối cộng này sẽ có 2 rãnh trống để lắp 2 giá trị.
<img width="592" height="611" alt="Screenshot 2026-06-08 215054" src="https://github.com/user-attachments/assets/7ff5ec60-1bc9-4475-8b7b-eb1c4bf35650" />

### Bước 2.4

Click `txtA`, kéo khối:

```text
txtA.Text
```

lắp vào rãnh thứ nhất của phép cộng.
<img width="576" height="653" alt="Screenshot 2026-06-08 215144" src="https://github.com/user-attachments/assets/e9bcb609-9c0b-451c-9b90-061ac80a07af" />

### Bước 2.5

Click `txtB`, kéo khối:

```text
txtB.Text
```

lắp vào rãnh thứ hai.

Logic:

```text
Khi bấm nút Tính
→ Lấy giá trị txtA
→ Cộng với giá trị txtB
→ Hiển thị kết quả lên lblKetQua
```
<img width="1919" height="1022" alt="Screenshot 2026-06-08 215243" src="https://github.com/user-attachments/assets/bd5b2a65-c1d3-40a3-908c-95241ba31706" />

---

# BƯỚC 3: XÂY DỰNG SCREEN 3 (Màn hình Web)

Tạo Screen mới:

```text
Add Screen
```

Đặt tên:

```text
Screen3
```

---

## 1. Phần Designer (Thiết kế giao diện)

### Bước 1.1

Nhìn sang Palette, tìm mục User Interface (hoặc Layout tùy phiên bản).

Kéo component:

```text
WebViewer
```

thả vào màn hình.

### Bước 1.2

Trong cột Properties của WebViewer, để cho trang web hiển thị tràn viền:

```text
Height = Fill parent
Width  = Fill parent
```
<img width="1919" height="1024" alt="Screenshot 2026-06-08 215406" src="https://github.com/user-attachments/assets/bf944e30-e02d-45b8-8e91-f3835dbb2e64" />

---

## 2. Phần Blocks (Lập trình logic)

### Bước 2.1

Chuyển sang Blocks.

Click vào chữ:

```text
Screen3
```

ở cột bên trái.

Kéo khối sự kiện:

```text
when Screen3.Initialize do
```

ra màn hình.
<img width="897" height="811" alt="Screenshot 2026-06-08 215730" src="https://github.com/user-attachments/assets/59aa79d0-92d2-4dc8-95af-84cbb2a46f97" />

> Sự kiện này tự động chạy ngay khi màn hình vừa được mở lên.

### Bước 2.2

Click vào `WebViewer1` ở cột bên trái.

Kéo khối màu tím:

```text
call WebViewer1.GoToUrl url
```

lắp vào bên trong.
<img width="677" height="672" alt="Screenshot 2026-06-08 215803" src="https://github.com/user-attachments/assets/ddb3ac8a-07ea-4487-8d57-e49194fe204e" />

### Bước 2.3

Vào mục Text (màu hồng), kéo khối:

```text
" "
```

lắp vào đuôi chữ:

```text
url
```
<img width="564" height="485" alt="Screenshot 2026-06-08 215839" src="https://github.com/user-attachments/assets/c0079022-9969-4db8-a95c-a5f546b9b972" />

### Bước 2.4

Gõ địa chỉ trang web mong muốn vào.

Ví dụ:

```text
https://k58kmt.tdh.io.vn
```

hoặc bất kỳ website nào khác.
<img width="769" height="340" alt="Screenshot 2026-06-08 215953" src="https://github.com/user-attachments/assets/557fe3d6-8ba1-4ccd-ba48-7a554df2fd87" />

---
# Test trực tiếp qua Wifi bằng MIT AI2 Companion

Đây là cách nhanh nhất và phổ biến nhất để chạy thử ứng dụng trên điện thoại. Điểm mạnh của phương pháp này là **không cần cài đặt APK vào máy**, đồng thời mọi thay đổi trên giao diện hoặc Blocks trong MIT App Inventor sẽ được cập nhật ngay lập tức trên điện thoại (**live reload**).

## Yêu cầu

* Điện thoại và máy tính phải kết nối cùng một mạng Wifi.
* Đã tạo xong project trên MIT App Inventor.

---

## Các bước thực hiện

### 1. Cài đặt ứng dụng MIT App Inventor trên điện thoại

#### Android

* Mở **CH Play**
* Tìm kiếm: **MIT App Inventor**
* Cài đặt ứng dụng

#### iPhone (iOS)

* Mở **App Store**
* Tìm kiếm: **MIT App Inventor**
* Cài đặt ứng dụng
<img width="290" height="496" alt="image" src="https://github.com/user-attachments/assets/9852a1c3-c79d-437b-94e4-6acf9c68c1c4" />

---

### 2. Mở chức năng kết nối trên máy tính

Trong giao diện MIT App Inventor:

* Chọn menu **Connect**
* Chọn **AI Companion**
<img width="533" height="400" alt="Screenshot 2026-06-08 220504" src="https://github.com/user-attachments/assets/be620bdd-5eb0-4d28-bf16-fa8f6cb7f682" />

Sau khi bấm, màn hình sẽ hiển thị:

* Một mã QR
* Một mã kết nối gồm 6 ký tự
<img width="1919" height="1022" alt="Screenshot 2026-06-08 220710" src="https://github.com/user-attachments/assets/c7aed823-ba8b-40ea-af9e-c3892d6026e3" />

---

### 3. Kết nối điện thoại với dự án

Mở ứng dụng **MIT AI2 Companion** trên điện thoại.

Có 2 cách kết nối:

#### Cách 1: Quét mã QR

* Chọn **Scan QR Code**
* Hướng camera vào mã QR trên màn hình máy tính

#### Cách 2: Nhập mã kết nối

* Nhập mã 6 ký tự được hiển thị trên màn hình
* Chọn **Connect with Code**
<img width="290" height="496" alt="image" src="https://github.com/user-attachments/assets/464b15b1-bde6-4e34-be96-059336e4f36b" />

---

### 4. Chạy thử ứng dụng

* Chờ vài giây để ứng dụng tải dữ liệu từ máy tính.
<img width="1919" height="1025" alt="Screenshot 2026-06-08 220723" src="https://github.com/user-attachments/assets/ba6b912b-389d-4d17-aa6c-06deed545332" />
  
* Sau khi kết nối thành công, **Screen1** của project sẽ xuất hiện trên điện thoại.
<img width="290" height="496" alt="image" src="https://github.com/user-attachments/assets/304376ee-d4d6-4143-ac7c-a67a6c109eba" />

Từ thời điểm này:

* Mọi thay đổi giao diện trong **Designer**
* Mọi chỉnh sửa logic trong **Blocks**

sẽ được cập nhật gần như ngay lập tức trên điện thoại mà không cần biên dịch lại ứng dụng.

---

## Ưu điểm của AI2 Companion

* Không cần tạo file APK để kiểm tra.
* Hỗ trợ Live Reload.
* Tiết kiệm thời gian phát triển.
* Dễ phát hiện và sửa lỗi.
* Phù hợp cho quá trình học tập và thử nghiệm ứng dụng.

---

## Kết quả mong đợi

Sau khi kết nối thành công:

* Hiển thị **Screen1 (About)** trên điện thoại.
* Có thể điều hướng sang:

  * **Screen2** (Giải toán)
<img width="290" height="496" alt="image" src="https://github.com/user-attachments/assets/eb78da8c-6563-4c72-8b54-baa0ff23276c" />

   * **Screen3** (Xem Web)
<img width="290" height="496" alt="image" src="https://github.com/user-attachments/assets/d69d5e7a-0856-4c51-9060-ce10100764cd" />

* Kiểm tra toàn bộ chức năng của ứng dụng trực tiếp trên thiết bị thật.
<img width="1156" height="552" alt="Screenshot 2026-06-08 225103" src="https://github.com/user-attachments/assets/47d978a7-cc44-4668-a1c6-3685fa894af5" />

