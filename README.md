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

# CÁCH TEST 2: Xuất file APK để cài đặt thật vào máy (Test độc lập)

Phương pháp này được sử dụng khi ứng dụng đã hoàn thiện và cần cài đặt trực tiếp lên điện thoại Android hoặc chia sẻ cho người khác sử dụng.

## Yêu cầu

* Điện thoại sử dụng hệ điều hành Android.
* Dự án đã được hoàn thành trên MIT App Inventor.
* Có kết nối Internet để thực hiện quá trình biên dịch và tải file APK.

---

## Các bước thực hiện

### 1. Biên dịch ứng dụng

Trong giao diện MIT App Inventor:

* Chọn menu **Build**
* Chọn **Android App (.apk)**

Hệ thống sẽ bắt đầu quá trình đóng gói ứng dụng.

---

### 2. Chờ quá trình biên dịch

MIT App Inventor sẽ:

* Tổng hợp giao diện (Designer)
* Tổng hợp các khối lệnh (Blocks)
* Đóng gói toàn bộ thành một file cài đặt Android (.apk)

Thời gian thực hiện thường từ **1–2 phút**, tùy theo độ phức tạp của ứng dụng.

---

### 3. Tải file APK

Sau khi biên dịch hoàn tất:

* Hệ thống sẽ hiển thị một mã QR.
* Đồng thời cung cấp liên kết tải trực tiếp file APK.

Có thể lựa chọn một trong hai cách:

#### Cách 1: Quét mã QR

* Mở camera hoặc ứng dụng quét mã QR trên điện thoại.
* Quét mã QR được hiển thị trên màn hình.
* Điện thoại sẽ tự động tải file APK.

#### Cách 2: Tải về máy tính

* Chọn **Download .apk**
* Lưu file APK về máy tính.
* Chép sang điện thoại bằng cáp USB, Bluetooth hoặc các dịch vụ lưu trữ đám mây.

---

### 4. Cài đặt ứng dụng

Sau khi tải xong:

* Mở file APK trên điện thoại.
* Chọn **Cài đặt (Install)**.

Nếu Android hiển thị cảnh báo:

> Cho phép cài đặt ứng dụng từ nguồn không xác định

Thực hiện:

* Chọn **Cài đặt từ nguồn này**
* Hoặc **Cho phép**
* Sau đó tiếp tục cài đặt.

---

### 5. Chạy ứng dụng

Sau khi cài đặt hoàn tất:

* Chọn **Mở (Open)**
* Hoặc tìm biểu tượng ứng dụng ngoài màn hình chính.

Ứng dụng sẽ hoạt động độc lập mà không cần kết nối với MIT App Inventor.

---

## Ưu điểm của việc xuất APK

* Có thể sử dụng ứng dụng mọi lúc mà không cần kết nối MIT App Inventor.
* Dễ dàng chia sẻ cho người khác.
* Có thể lưu trữ lâu dài trên điện thoại.
* Phù hợp cho việc nộp bài tập, trình diễn sản phẩm hoặc triển khai thực tế.

---

## Kết quả mong đợi

Sau khi cài đặt thành công:

* Ứng dụng xuất hiện trên màn hình điện thoại.
* Có thể mở và sử dụng như một ứng dụng Android thông thường.
* Hoạt động độc lập, không phụ thuộc vào trình duyệt hoặc MIT AI2 Companion.

---

# PHẦN 2: LÝ THUYẾT ANDROID STUDIO
<img width="225" height="225" alt="image" src="https://github.com/user-attachments/assets/a3eaf171-5665-4cb0-b358-46879d99b2d4" />

https://developer.android.com/?hl=vi

## 1. AndroidManifest.xml và Quyền (Permissions)

### AndroidManifest.xml là gì?
<img width="642" height="513" alt="image" src="https://github.com/user-attachments/assets/eb18f351-c296-47a0-8764-92b73212e9cf" />

`AndroidManifest.xml` là tập tin cấu hình quan trọng nhất của một ứng dụng Android. Có thể xem đây là "chứng minh thư" của ứng dụng, nơi khai báo:

* Tên ứng dụng
* Biểu tượng (Icon)
* Các Activity (màn hình)
* Các Service
* Các Broadcast Receiver
* Các quyền (Permissions) mà ứng dụng cần sử dụng

### Khai báo quyền

Ví dụ khai báo quyền truy cập Internet:

```xml
<uses-permission android:name="android.permission.INTERNET" />
```

Thẻ này được đặt bên trong thẻ `<manifest>`.

### Mục đích của Permissions

* Cho hệ điều hành biết ứng dụng cần truy cập tài nguyên nào.
* Bảo vệ quyền riêng tư của người dùng.
* Hiển thị cảnh báo hoặc hộp thoại xin quyền khi cần thiết.

---

## 2. Vòng đời ứng dụng và hàm onCreate()

### Vòng đời Activity

Một Activity thông thường sẽ trải qua các trạng thái sau:

```text
onCreate()
    ↓
onStart()
    ↓
onResume()
    ↓
(Tương tác với người dùng)
    ↓
onPause()
    ↓
onStop()
    ↓
onDestroy()
```

### Hàm onCreate()

Đây là hàm đầu tiên được Android gọi khi Activity được khởi tạo.

Ví dụ:

```java
@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);
}
```

### Vai trò của onCreate()

* Gắn giao diện XML vào Activity.
* Khởi tạo biến.
* Ánh xạ View.
* Thiết lập sự kiện.
* Chuẩn bị dữ liệu ban đầu.

Có thể xem `onCreate()` tương đương với hàm `main()` trong các chương trình Java cơ bản.

---

## 3. Xin quyền Runtime bằng Java

Từ Android 6.0 (API 23) trở lên, ngoài việc khai báo trong Manifest, ứng dụng còn phải xin quyền khi đang chạy.

Ví dụ kiểm tra quyền Camera:

```java
if (ContextCompat.checkSelfPermission(
        this,
        Manifest.permission.CAMERA)
        != PackageManager.PERMISSION_GRANTED) {

    ActivityCompat.requestPermissions(
            this,
            new String[]{Manifest.permission.CAMERA},
            100);
}
```

### Ý nghĩa

* Kiểm tra xem quyền đã được cấp chưa.
* Nếu chưa có quyền, hiển thị hộp thoại xin phép người dùng.
* Người dùng có thể đồng ý hoặc từ chối.

Việc này giúp tăng tính bảo mật và bảo vệ dữ liệu cá nhân.

---

## 4. Giao diện Android (XML Layout)

### Thư mục Layout

Các file giao diện được đặt trong:

```text
res/layout/
```

Ví dụ:

```text
activity_main.xml
activity_login.xml
activity_about.xml
```

---

### Tham chiếu tài nguyên (Resources)

Không nên ghi trực tiếp nội dung văn bản vào XML.

#### Không khuyến khích

```xml
android:text="Xin chào"
```

#### Khuyến khích

Trong file:

```text
res/values/strings.xml
```

```xml
<string name="hello_msg">Xin chào</string>
```

Sau đó gọi:

```xml
android:text="@string/hello_msg"
```

---

### Gọi trong Java

```java
getString(R.string.hello_msg);
```

Ví dụ:

```java
TextView tv = findViewById(R.id.tvHello);
tv.setText(getString(R.string.hello_msg));
```

---

### Ưu điểm

* Dễ bảo trì.
* Tránh lặp dữ liệu.
* Hỗ trợ đa ngôn ngữ.
* Hỗ trợ giao diện tối (Dark Mode).

---

### Auto Language

Ví dụ:

```text
values/
values-vi/
values-en/
```

Android sẽ tự động chọn ngôn ngữ phù hợp theo thiết bị.

---

### Auto Theme

Ví dụ:

```text
values/
values-night/
```

Khi người dùng bật Dark Mode, Android sẽ tự động sử dụng tài nguyên trong thư mục `values-night`.

---

### LinearLayout

Là một ViewGroup dùng để chứa các View khác.

#### Sắp xếp theo chiều dọc

```xml
android:orientation="vertical"
```

#### Sắp xếp theo chiều ngang

```xml
android:orientation="horizontal"
```

---

### Gravity

Căn chỉnh nội dung bên trong Layout.

Ví dụ:

```xml
android:gravity="center"
```

Các giá trị thường dùng:

```text
center
left
right
top
bottom
center_horizontal
center_vertical
```

---

## 5. Tương tác với Layout bằng Code

### Ánh xạ View

Ví dụ:

```java
TextView myText =
        findViewById(R.id.text_view_id);
```

### Thay đổi nội dung

```java
myText.setText(R.string.hello_msg);
```

Ưu điểm:

* Không hardcode văn bản.
* Android tự chọn ngôn ngữ phù hợp.
* Dễ quản lý nội dung.

---

## 6. Sự kiện Click (Event Click)

Android hỗ trợ nhiều cách xử lý sự kiện.

---

### Cách 1: Khai báo trong XML

Trong Layout:

```xml
<Button
    android:id="@+id/btnTinh"
    android:onClick="tinhToan"
    android:text="Tính" />
```

Trong Java:

```java
public void tinhToan(View v) {
    // Xử lý sự kiện
}
```

---

### Cách 2: Đăng ký Listener bằng Java (Khuyến khích)

Ánh xạ Button:

```java
Button btn =
        findViewById(R.id.my_btn);
```

Gắn Listener:

```java
btn.setOnClickListener(
    new View.OnClickListener() {

        @Override
        public void onClick(View v) {

            // Thực hiện hành động

        }
    }
);
```

### Ưu điểm

* Dễ quản lý mã nguồn.
* Tách biệt giao diện và logic.
* Phù hợp với dự án lớn.
* Dễ mở rộng và bảo trì.

---

## Kết luận

Sau phần lý thuyết này cần nắm được:

* Vai trò của AndroidManifest.xml.
* Cách khai báo và xin quyền Runtime.
* Vòng đời của Activity và hàm onCreate().
* Cách xây dựng giao diện bằng XML.
* Cách sử dụng tài nguyên Strings.
* Khái niệm Layout và ViewGroup.
* Cách tương tác với giao diện bằng Java.
* Hai phương pháp xử lý sự kiện Click trong Android Studio.

---

# PHẦN 3: APP 1 - XỬ LÝ DỮ LIỆU TỪ THƯ MỤC ASSETS

## 1. Kiến thức về Assets

### Cú pháp truy cập:

```java
AssetManager assetManager = getAssets();
InputStream is = assetManager.open("ninh_data.txt");
```

Lợi ích: Đóng gói sẵn dữ liệu (Database ban đầu, file cấu hình, JSON, hình ảnh, âm thanh) trực tiếp vào file APK/AAB. App vẫn hoạt động bình thường, load cực nhanh dù không có Internet.

Ứng dụng: Làm app từ điển offline, app sách truyện, cẩm nang du lịch, hoặc app chứa sẵn tệp trọng số (weights file) của mạng nơ-ron CNN.

## 2. App 1: "Cẩm nang TNUT Offline"

Vấn đề đặt ra: Sinh viên cần xem danh sách các phòng ban và thông báo nội bộ của trường, nhưng mạng KTX đôi lúc chập chờn.

Dữ liệu (Đặc thù): File cam_nang.json chứa cấu trúc danh sách, được copy sẵn vào thư mục src/main/assets/. Dữ liệu tĩnh, có cấu trúc phân tầng.

Thuật toán xử lý:

1. Đọc luồng byte (InputStream) từ file cam_nang.json.
2. Sử dụng vòng lặp StringBuilder để gom các byte lại thành chuỗi String hoàn chỉnh.
3. Dùng lớp JSONObject và JSONArray để tiền xử lý, bóc tách chuỗi String đó thành danh sách các Object thực thể trong Java.

Đối tượng hiển thị: Sử dụng RecyclerView kết hợp với CardView để hiển thị danh sách các mục thật đẹp mắt, tối ưu bộ nhớ khi cuộn màn hình.

---

Dưới đây là 5 bước để hiện thực hóa ứng dụng này:

# BƯỚC 1: TẠO THƯ MỤC ASSETS VÀ CHUẨN BỊ DỮ LIỆU

## 1. Khởi tạo Project:

Mở Android Studio, tạo một dự án mới (Empty Views Activity), đặt tên là CamNangTNUT, ngôn ngữ chọn Java.
<img width="772" height="689" alt="Screenshot 2026-06-08 232310" src="https://github.com/user-attachments/assets/db19647e-003e-4d47-a505-9cbe893ae9a7" />

## 2. Tạo thư mục Assets:

Trong cửa sổ Project bên trái (để chế độ xem là Android), nhấn chuột phải vào thư mục app -> Chọn New -> Folder -> Assets Folder.
<img width="1919" height="1079" alt="Screenshot 2026-06-08 232906" src="https://github.com/user-attachments/assets/2ed7212c-0f71-41ea-a72a-bccf9a80177a" />

Một hộp thoại hiện ra, cứ giữ nguyên các tùy chọn mặc định và bấm Finish. Thư mục assets màu vàng sẽ xuất hiện bên trong thư mục main.
<img width="304" height="275" alt="Screenshot 2026-06-08 232932" src="https://github.com/user-attachments/assets/f4dab844-c441-49a5-b31c-04b60fa6dfbc" />

## 3. Tạo file dữ liệu JSON:

Nhấn chuột phải vào thư mục assets vừa tạo -> New -> File. Đặt tên là cam_nang.json.

Mở file này lên và dán đoạn dữ liệu chuẩn bị trước này vào (đây là định dạng JSON rất phổ biến):

```json
[
  {
    "tieu_de": "Văn phòng Khoa Điện tử",
    "noi_dung": "Nơi hỗ trợ các vấn đề học tập cho sinh viên KMT."
  },
  {
    "tieu_de": "Phòng Đào tạo TNUT",
    "noi_dung": "Tầng 1 Toà nhà Trung tâm. Giải đáp thắc mắc về tín chỉ, học phí."
  },
  {
    "tieu_de": "Ký túc xá TNUT",
    "noi_dung": "Khu vực lưu trú của sinh viên. Báo cáo hỏng hóc cơ sở vật chất tại Ban Quản lý."
  }
]
```
<img width="1919" height="1079" alt="Screenshot 2026-06-08 233327" src="https://github.com/user-attachments/assets/81415ded-dc2a-4469-b136-5114919352c7" />

# BƯỚC 2: THIẾT KẾ GIAO DIỆN (XML)

Chúng ta cần 2 file giao diện: 1 cho màn hình chính, 1 cho từng thẻ thông tin (Card) hiển thị trong danh sách.

## 1. File màn hình chính (res/layout/activity_main.xml):

Thay thế toàn bộ code cũ bằng code sau để tạo một danh sách cuộn RecyclerView:

```xml
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:background="#F5F5F5"
    android:padding="16dp">

    <TextView
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Cẩm nang Sinh Viên"
        android:textSize="24sp"
        android:textStyle="bold"
        android:gravity="center"
        android:layout_marginBottom="16dp" />

    <androidx.recyclerview.widget.RecyclerView
        android:id="@+id/rvCamNang"
        android:layout_width="match_parent"
        android:layout_height="match_parent" />
</LinearLayout>
```
<img width="1919" height="1079" alt="Screenshot 2026-06-08 233756" src="https://github.com/user-attachments/assets/d7941418-b315-4b8c-93e0-5b97876b24c3" />

## 2. File thiết kế từng thẻ thông tin (res/layout/item_cam_nang.xml):

Chuột phải vào thư mục res/layout -> New -> Layout Resource File -> Đặt tên là item_cam_nang.
<img width="1025" height="628" alt="Screenshot 2026-06-08 234026" src="https://github.com/user-attachments/assets/3a233dd7-fbdd-40dd-a7a2-86b67c3efda5" />

```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.cardview.widget.CardView xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="wrap_content"
    android:layout_marginBottom="12dp"
    app:cardCornerRadius="8dp"
    app:cardElevation="4dp">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        android:padding="16dp">

        <TextView
            android:id="@+id/tvTieuDe"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:textSize="18sp"
            android:textStyle="bold"
            android:textColor="#000000" />

        <TextView
            android:id="@+id/tvNoiDung"
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_marginTop="8dp"
            android:textSize="14sp"
            android:textColor="#555555" />
    </LinearLayout>
</androidx.cardview.widget.CardView>
```
<img width="1919" height="1079" alt="Screenshot 2026-06-08 234047" src="https://github.com/user-attachments/assets/28dddda9-cbd2-463d-b35d-2e2adbaf2bb0" />

# BƯỚC 3: TẠO CLASS MODEL VÀ ADAPTER (XỬ LÝ DỮ LIỆU)

Để RecyclerView hoạt động, nó cần một "bộ chuyển đổi" (Adapter) để nhét dữ liệu từ Java vào giao diện XML.

## 1. Tạo Model Class (CamNang.java):

Chuột phải vào thư mục package chứa code Java của ngài -> New -> Java Class -> Đặt tên CamNang.

```java
package com.example.camnangtnut;
public class CamNang {
    private String tieuDe;
    private String noiDung;

    public CamNang(String tieuDe, String noiDung) {
        this.tieuDe = tieuDe;
        this.noiDung = noiDung;
    }

    public String getTieuDe() { return tieuDe; }
    public String getNoiDung() { return noiDung; }
}
```
<img width="1919" height="1079" alt="Screenshot 2026-06-08 234651" src="https://github.com/user-attachments/assets/906d7a05-be78-4666-80a7-b3c3ec5f03e4" />

## 2. Tạo Adapter (CamNangAdapter.java):

Tạo Class mới tên CamNangAdapter. Đoạn code này khá tiêu chuẩn, ngài chỉ cần sao chép và dán:

```java
package com.example.camnangtnut;
import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.TextView;
import androidx.annotation.NonNull;
import androidx.recyclerview.widget.RecyclerView;
import java.util.List;

public class CamNangAdapter extends RecyclerView.Adapter<CamNangAdapter.ViewHolder> {

    private List<CamNang> listData;

    public CamNangAdapter(List<CamNang> listData) {
        this.listData = listData;
    }

    @NonNull
    @Override
    public ViewHolder onCreateViewHolder(@NonNull ViewGroup parent, int viewType) {
        // Gắn layout item_cam_nang.xml vào mỗi dòng
        View view = LayoutInflater.from(parent.getContext()).inflate(R.layout.item_cam_nang, parent, false);
        return new ViewHolder(view);
    }

    @Override
    public void onBindViewHolder(@NonNull ViewHolder holder, int position) {
        // Lấy dữ liệu và đổ vào UI
        CamNang item = listData.get(position);
        holder.tvTieuDe.setText(item.getTieuDe());
        holder.tvNoiDung.setText(item.getNoiDung());
    }

    @Override
    public int getItemCount() {
        return listData.size();
    }

    public static class ViewHolder extends RecyclerView.ViewHolder {
        TextView tvTieuDe, tvNoiDung;
        public ViewHolder(@NonNull View itemView) {
            super(itemView);
            tvTieuDe = itemView.findViewById(R.id.tvTieuDe);
            tvNoiDung = itemView.findViewById(R.id.tvNoiDung);
        }
    }
}
```
<img width="1919" height="1079" alt="Screenshot 2026-06-08 235011" src="https://github.com/user-attachments/assets/e6f69c3e-a1c7-41df-a9fd-0fe3b384ecec" />

# BƯỚC 4: GHÉP NỐI TẠI MAIN ACTIVITY (THUẬT TOÁN LÕI)

Đây là nơi đọc file từ assets và hiển thị lên màn hình. Mở file MainActivity.java và viết code như sau:

```java
package com.example.camnangtnut;
import androidx.appcompat.app.AppCompatActivity;
import androidx.recyclerview.widget.LinearLayoutManager;
import androidx.recyclerview.widget.RecyclerView;
import android.os.Bundle;
import org.json.JSONArray;
import org.json.JSONObject;
import java.io.InputStream;
import java.util.ArrayList;
import java.util.List;

public class MainActivity extends AppCompatActivity {

    private RecyclerView rvCamNang;
    private CamNangAdapter adapter;
    private List<CamNang> danhSachCamNang;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        rvCamNang = findViewById(R.id.rvCamNang);
        rvCamNang.setLayoutManager(new LinearLayoutManager(this));

        danhSachCamNang = new ArrayList<>();

        // 1. Thực thi hàm đọc và xử lý dữ liệu
        docDuLieuTuAssets();

        // 2. Cài đặt Adapter cho RecyclerView
        adapter = new CamNangAdapter(danhSachCamNang);
        rvCamNang.setAdapter(adapter);
    }

    // THUẬT TOÁN XỬ LÝ DỮ LIỆU JSON
    private void docDuLieuTuAssets() {
        try {
            // Mở luồng đọc file từ thư mục assets
            InputStream is = getAssets().open("cam_nang.json");

            // Tính toán kích thước file và đưa vào bộ đệm byte
            int size = is.available();
            byte[] buffer = new byte[size];
            is.read(buffer);
            is.close();

            // Chuyển mảng byte thành chuỗi String (UTF-8)
            String jsonChuoi = new String(buffer, "UTF-8");

            // Phân tích chuỗi JSON thành mảng (Array)
            JSONArray jsonArray = new JSONArray(jsonChuoi);

            // Vòng lặp bóc tách từng đối tượng và nhét vào List của Java
            for (int i = 0; i < jsonArray.length(); i++) {
                JSONObject obj = jsonArray.getJSONObject(i);
                String tieuDe = obj.getString("tieu_de");
                String noiDung = obj.getString("noi_dung");

                danhSachCamNang.add(new CamNang(tieuDe, noiDung));
            }

        } catch (Exception e) {
            e.printStackTrace(); // Bắt lỗi nếu file không tồn tại hoặc sai định dạng JSON
        }
    }
}
```
<img width="1919" height="1079" alt="Screenshot 2026-06-08 235107" src="https://github.com/user-attachments/assets/b8a457cd-fcca-4b90-98de-baf37b0a6def" />

# BƯỚC 5: CHẠY THỬ VÀ TẬN HƯỞNG
Ứng dụng này hoàn toàn Offline, giải quyết triệt để yêu cầu đọc file từ Assets, không cần bất kỳ đường truyền mạng nào!
## CÁCH 1: Tạo máy ảo (Emulator) ngay trên máy tính

Sẽ tạo ra một chiếc "điện thoại giả" nằm ngay trên màn hình máy tính để xem app.

### Bước 1:
Nhìn lên thanh công cụ trên cùng của Android Studio, tìm và bấm vào biểu tượng Device Manager (thường có hình một chiếc điện thoại nhỏ với logo Android, hoặc nằm ở thanh viền mép bên phải màn hình).

<img width="283" height="379" alt="Screenshot 2026-06-08 235519" src="https://github.com/user-attachments/assets/2f2a0169-8d0e-42be-8f8d-7669d9ca6a68" />

### Bước 2:
Một bảng điều khiển hiện ra, bấm vào nút Create device (Tạo thiết bị) hoặc biểu tượng dấu cộng +.

<img width="292" height="169" alt="Screenshot 2026-06-08 235613" src="https://github.com/user-attachments/assets/f7100a2f-df89-47c3-b3cf-e163994a1857" />

### Bước 3:
Bảng chọn phần cứng hiện ra, cứ tuỳ ý chọn một dòng máy (Ví dụ: Pixel 6 hoặc Pixel 7) rồi bấm Next.
<img width="1919" height="1079" alt="Screenshot 2026-06-08 235644" src="https://github.com/user-attachments/assets/fc59577e-1de7-4e4b-bdab-8ec71f1ea9c5" />

### Bước 4:
Bảng chọn hệ điều hành hiện ra (System Image). Ở tab Recommended, hãy bấm vào biểu tượng Mũi tên tải xuống (Download) ở cạnh một phiên bản bất kỳ (Ví dụ: Tiramisu hoặc UpsideDownCake).
<img width="1130" height="861" alt="Screenshot 2026-06-08 235832" src="https://github.com/user-attachments/assets/09a9e40b-446b-42fd-a2d8-df086bf16f74" />
<img width="1117" height="810" alt="Screenshot 2026-06-08 235928" src="https://github.com/user-attachments/assets/4e009150-b3a1-434e-92f1-678e3f469a63" />

**Lưu ý:** Quá trình tải này khoảng 1GB, đợi một chút cho nó tải xong rồi bấm Finish.

### Bước 5:
Sau khi tải xong hệ điều hành, chọn vào nó rồi bấm Next -> Finish.

### Bước 6:
Đóng bảng Device Manager lại. Lúc này, nhìn lên thanh công cụ (ngay cạnh cái nút Run màu xanh lá ngài vừa bấm), sẽ thấy tên chiếc máy ảo vừa tạo xuất hiện. Chỉ việc bấm Run lại một lần nữa và chiêm ngưỡng thành quả của mình hiển thị trên máy ảo!
<img width="1919" height="1079" alt="Screenshot 2026-06-09 000654" src="https://github.com/user-attachments/assets/1881c381-6a0c-47fc-8c7c-f6384f827fb9" />
<img width="527" height="1019" alt="Screenshot 2026-06-09 000900" src="https://github.com/user-attachments/assets/ebb3e06d-9677-4a51-90ff-a8a0b3dfb95e" />

---

## CÁCH 2: Chạy trực tiếp trên điện thoại Android thật 

### Bước 1:
Dùng cáp USB xịn để cắm nối điện thoại Android vào máy tính.

### Bước 2:
Cầm điện thoại lên, vào **Cài đặt -> Giới thiệu về điện thoại -> Bấm liên tục 7 lần vào dòng Số hiệu bản tạo (Build number)** cho đến khi máy báo **"Bạn đã là nhà phát triển!"**.

### Bước 3:
Quay lại màn hình Cài đặt chính, tìm mục **Tùy chọn nhà phát triển (Developer options)** vừa xuất hiện.

### Bước 4:
Tìm đến dòng **Gỡ lỗi USB (USB debugging)** và gạt nút bật nó lên.

### Bước 5:
Trên màn hình điện thoại lúc này sẽ hiện một bảng hỏi **"Cho phép gỡ lỗi USB từ máy tính này?"**, bấm **Cho phép (OK)**.

### Bước 6:
Ngước nhìn lên màn hình Android Studio, sẽ thấy tên chiếc điện thoại thật của mình hiện ra cạnh nút Run. Bấm Run và app sẽ tự động cài thẳng vào máy!
