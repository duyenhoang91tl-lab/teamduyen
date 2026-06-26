# OME Zalo AI Helper - Chrome Extension

## Cài đặt (1 lần duy nhất)

1. Mở Chrome → vào địa chỉ: `chrome://extensions`
2. Bật **Developer mode** (góc trên phải)
3. Nhấn **Load unpacked** → chọn thư mục `zalo-extension`
4. Extension đã cài xong ✓

## Sử dụng

1. Mở `chat.zalo.me` trong Chrome
2. Nhấn nút **🤖 AI** ở cạnh phải màn hình để mở panel
3. Lần đầu: nhấn ⚙ để cài đặt:
   - **URL Web App GAS**: lấy từ app teamduyen (URL dạng `https://script.google.com/macros/s/.../exec`)
   - **Gemini API Key**: lấy miễn phí tại https://aistudio.google.com/app/apikey
4. Khi mở chat với khách:
   - Extension tự động phát hiện SĐT từ tên chat (nếu tên có số điện thoại)
   - Hoặc nhập tay SĐT → nhấn **Tra cứu**
5. Xem lịch sử đơn hàng + tình trạng CS
6. Dán tin nhắn của khách → chọn giọng văn → nhấn **✨ Tạo gợi ý AI**
7. Click vào gợi ý để copy → paste vào Zalo

## Đồng bộ tình trạng về app

- Sau khi tra cứu khách, phần **Cập nhật tình trạng CS** sẽ hiện ra
- Chỉnh trạng thái + ghi chú → nhấn **💾 Lưu về GSheet**
- Dữ liệu được ghi thẳng vào Google Sheets (qua GAS `action=saveSingle`)
- App teamduyen sẽ thấy ngay sau khi Sync GS

## Lưu ý

- SĐT tự động phát hiện khi tên chat Zalo có chứa 10 số (VD: "0901234567 - Nguyễn Văn A")
- Cache dữ liệu 5 phút, tự động tải lại
- Gemini API Free: 15 yêu cầu/phút, 1 triệu token/ngày — đủ dùng
