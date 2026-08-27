# Robot sự kiện — Hội nghị Xúc tiến đầu tư tỉnh Tây Ninh 2026

Phần mềm chạy trên robot **GreetingBot Nova** tại Hội trường Thống Nhất, UBND tỉnh Tây Ninh,
chiều **28/08/2026**.

| | |
|---|---|
| **File cài** | [`su-kien-xtdt-tay-ninh-v1.0.apk`](su-kien-xtdt-tay-ninh-v1.0.apk) — 8,41 MB |
| **Cài từ máy Windows** | [`Huong-dan-cai-APK-tu-Windows.pdf`](Huong-dan-cai-APK-tu-Windows.pdf) — 7 trang, có cả phần xử lý sự cố |
| **Cài từ MacBook** | [`Huong-dan-cai-APK-tu-MacBook.pdf`](Huong-dan-cai-APK-tu-MacBook.pdf) — 7 trang, có cả phần xử lý sự cố |
| **Đặt 9 điểm trên bản đồ** | [`Huong-dan-dat-diem-tren-ban-do.pdf`](Huong-dan-dat-diem-tren-ban-do.pdf) — 9 trang, có sơ đồ hướng robot đứng và bảng kiểm cuối cùng |
| Đơn vị cung cấp | Công ty Cổ phần Tập đoàn Roboworld — hotline **0866 153 946** |

---

## Tải về

GitHub không xem trước được file APK và PDF. Bấm vào tên file, rồi bấm nút
**Download raw file** (mũi tên tải xuống, góc trên bên phải).

Hoặc tải cả kho: nút **Code → Download ZIP**.

## Cài nhanh (đã có adb)

```bash
adb devices                                    # phải thấy dòng "device"
adb install -r su-kien-xtdt-tay-ninh-v1.0.apk  # đợi chữ "Success"
```

**Rồi mở app TỪ MÀN HÌNH CHÍNH CỦA ROBOT** — chạm vào biểu tượng ứng dụng.

> ⚠ **Đừng mở app bằng lệnh `adb shell am start`.** Mở kiểu đó thì robot không uỷ quyền
> cho app: mất cả dẫn đường lẫn giọng nói, mà **app không báo lỗi gì cả** — nhìn vẫn thấy
> giao diện bình thường.

Chưa có adb → mở PDF hướng dẫn cài đặt hợp với máy của mình (Windows hay MacBook), làm từ đầu.

> ⚠ Trên Windows, đừng gõ `adb` trần: máy nào từng cài phần mềm PUDU thì `C:\Windows\adb.exe`
> là bản cũ 1.0.39 và hai bản adb sẽ giết tiến trình của nhau. Xem mục A3 của PDF Windows.

## Bốn chức năng của app

| | Robot làm gì |
|---|---|
| **Xem thông tin sự kiện** | 13 mục bấm xem — chương trình, khu triển lãm, hướng dẫn đại biểu. Robot đọc thành tiếng |
| **Trò chuyện cùng tôi** | Hỏi bằng lời hoặc gõ chữ. Đây là nơi **duy nhất** micro bật |
| **Chế độ du hành** | Robot đi vòng quanh 5 điểm, vừa đi vừa chào mừng đại biểu |
| **Chế độ giới thiệu** | Dẫn đoàn tới từng điểm và thuyết minh. Xong mỗi điểm chờ bấm **Tiếp tục** |

## Trước khi chạy: đặt 9 điểm trên bản đồ

Hai chế độ di chuyển chỉ chạy khi robot đã quét bản đồ và có đủ 9 điểm, **tên trùng từng ký tự**:

```
Diem 1   Diem 2   Diem 3   Diem 4   Diem 5      ← chế độ du hành
Gioi thieu 1   Gioi thieu 2   Gioi thieu 3   Gioi thieu 4   ← chế độ giới thiệu
```

Không dấu tiếng Việt, đúng hoa/thường, đúng một dấu cách. Sai một ký tự là robot đứng im.

**Cách đặt, đặt ở đâu, quay mặt hướng nào** → xem [`Huong-dan-dat-diem-tren-ban-do.pdf`](Huong-dan-dat-diem-tren-ban-do.pdf).

**Tự kiểm:** ở màn hình chính của app, **bấm giữ nút 🏠 góc phải 1,2 giây** — bảng kiểm hiện
ra, hỏi thẳng robot và đánh dấu ✔/✘ từng điểm. Đừng nhìn bằng mắt trên màn quét bản đồ.

## Hai thứ hay quên

- **Âm lượng robot** — đã có lần bị kéo về 0. Nghe thử bằng tai, đừng nhìn thanh trượt.
- **Nút "Bật microphone"** trên dải trạng thái đỉnh màn hình robot: nếu có **gạch chéo** thì
  micro đang tắt ở cài đặt máy, app không tự bật được — phải chạm vào chính nút đó.

Và một điều kiện không sửa được bằng phần mềm: **người nói phải đứng đối diện robot**,
cách khoảng một mét. Robot dùng camera để biết ai đang nói với nó; đứng cạnh sườn hoặc nói
vọng từ xa thì nó bỏ qua.
