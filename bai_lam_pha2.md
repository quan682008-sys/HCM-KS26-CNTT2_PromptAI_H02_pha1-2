# BÀI LÀM PHA 2 – HACKATHON 02

- **Mã đề:** 07
- **Họ tên:**
- **Lớp:**
- **Link repository Pha2:**
- **Công cụ AI đã dùng (ChatGPT/Claude/Gemini):**

> Pha 2 (20 phút cuối). Mỗi mục: mở cuộc trò chuyện mới, gửi nguyên văn prompt đã viết trong bai_lam_pha1.md, dán câu trả lời và link chia sẻ vào đây. Xong, kéo thả file này vào repository Pha2.

## 4.2. Trích xuất tin nhắn đặt vé vào cổng ra JSON

**KET QUA AI**

```text
[
  {
    "loai_ve": "VECH",
    "ngay_choi": "2026-12-20",
    "nguoi_lon": 2,
    "tre_em": 1,
    "loai_tu": "nho",
    "ghi_chu": null
  },
  {
    "loai_ve": "VECN",
    "ngay_choi": "2027-01-03",
    "nguoi_lon": 3,
    "tre_em": 0,
    "loai_tu": null,
    "ghi_chu": "Một người đang bó bột tay"
  },
  {
    "loai_ve": "VEVIP",
    "ngay_choi": null,
    "nguoi_lon": 4,
    "tre_em": 0,
    "loai_tu": "lon",
    "ghi_chu": "một bạn đi xe lăn"
  }
]
```

**Link trò chuyện:https://share.gemini.google/UDV0hWUdL9rN**

## 4.3. Báo giá bằng Chain-of-Thought

**KET QUA AI**

```text
Bước 1: Tính tiền vé người lớnĐoàn mua vé cả ngày (VECN) với đơn giá 250.000 đồng/vé cho 8 người lớn:$$8 \times 250.000 = 2.000.000\text{ đồng}$$Bước 2: Tính tiền vé trẻ emCó 4 trẻ em cao từ 1 m đến 1,4 m (1,05 m; 1,15 m; 1,2 m; 1,3 m) áp dụng mức giá 60% vé người lớn:$$250.000 \times 60\% = 150.000\text{ đồng/vé}$$$$4 \times 150.000 = 600.000\text{ đồng}$$Có 2 bé cao dưới 1 m được miễn phí ($0\text{ đồng}$):$$2 \times 0 = 0\text{ đồng}$$Tổng tiền vé trẻ em:$$600.000 + 0 = 600.000\text{ đồng}$$Bước 3: Tính tiền giảm giá đoànTổng tiền vé trước giảm:$$2.000.000 + 600.000 = 2.600.000\text{ đồng}$$Vì đoàn có đủ 8 người lớn nên được giảm 10% trên tổng tiền vé:$$2.600.000 \times 10\% = 260.000\text{ đồng}$$Tiền vé sau khi giảm giá:$$2.600.000 - 260.000 = 2.340.000\text{ đồng}$$Bước 4: Tính tiền phụ thuĐoàn thuê 6 áo phao với giá 40.000 đồng/chiếc (không áp dụng giảm giá):$$6 \times 40.000 = 240.000\text{ đồng}$$Bước 5: Tính tổng tiềnTổng tiền = Tiền vé sau giảm + Tiền phụ thu:$$2.340.000 + 240.000 = 2.580.000\text{ đồng}$$[RESULT:2.580.000đồng]
```

**Link trò chuyện:https://share.gemini.google/dE8nwjMFwVbR**

### b) Kiểm tra kết quả AI



## 4.4. Dây chuyền xử lý khiếu nại – kết quả Trạm 1

**KET QUA AI**

```text
{
  "loai_su_co": "dong_khu_choi",
  "so_khach": 4,
  "so_khu_bi_dong": 2,
  "tom_tat": "Gia đình 4 người phản ánh khu trượt nước và khu sóng nhân tạo đóng cửa cả ngày không báo trước."
}
```

**Link trò chuyện:https://share.gemini.google/F0NOQVg50d8o**

## 4.5. Prompt chấm bài theo Rubric

**KET QUA AI**

```text
Tiêu chí	Điểm	Minh chứng	Đề xuất sửa
Đúng thông tin (50%)	0 / 5.0	
- Câu bị lỗi 1: "Vé chiều bên em 150k thôi ạ"


- Lí do sai: Báo sai giá vé VECH chuẩn của công ty (180.000 đồng/vé người lớn).



- Câu bị lỗi 2: "Mưa mà đóng cửa thì bên em hoàn tiền mặt 100% cho chị nha."


- Lí do sai: Báo sai chính sách hoàn/bù vé. Công ty không hoàn tiền mặt; khách đã vào dưới 2 giờ được tặng 1 vé cùng loại dùng trong 30 ngày, từ 2 giờ trở lên không được bù.

"Dạ, giá vé VECH (vé chiều) hiện tại là 180.000 đồng/vé người lớn ạ. Trong trường hợp phải đóng cửa do thời tiết xấu: nếu chị đã vào cổng dưới 2 giờ, bên em sẽ tặng lại 1 vé cùng loại có hạn sử dụng trong 30 ngày (không áp dụng hoàn tiền mặt); nếu đã vào từ 2 giờ trở lên sẽ không áp dụng chính sách bù vé ạ."
Đầy đủ (30%)	2.0 / 3.0	
- Câu bị lỗi: "Cần gì ới em nhé!" (thiếu thông tin điều hướng chốt đơn).


- Lí do sai: Đã trả lời đủ 2 ý hỏi về giá và chính sách mưa, nhưng thiếu lời mời khách hàng cung cấp ngày đi chơi và số lượng vé để hỗ trợ đặt vé.

"Chị dự định đi vào ngày nào và cần đặt bao nhiêu vé để em hỗ trợ giữ vé cho mình ngay ạ?"
Giọng điệu (20%)	0.5 / 2.0	
- Câu bị lỗi: "Hello chị!", "150k", "mát rượi luôn", "nha", "Cần gì ới em nhé!"


- Lí do sai: Sử dụng nhiều từ ngữ suồng sã, thiếu tính chuyên nghiệp trong giao tiếp chăm sóc khách hàng ("Hello", "k", "mát rượi luôn", "ới").

"Dạ em chào chị ạ!", thay "150k" bằng "180.000 đồng", lược bỏ cụm "mát rượi luôn", và thay "Cần gì ới em nhé!" bằng "Nếu cần hỗ trợ thêm thông tin gì, chị cứ nhắn cho em nhé ạ."
Tổng điểm	2.5 / 10
```

**Link trò chuyện:https://share.gemini.google/Z9VrlAlVBgEG**
