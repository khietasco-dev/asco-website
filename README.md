# Website ASCO — bản thiết kế lại

Nguyên mẫu website nhiều trang cho **Hãng Kiểm toán và Định giá ASCO**, thay cho trang asco.vn hiện tại.
HTML tĩnh, mỗi trang là một file độc lập, không cần máy chủ hay cơ sở dữ liệu.

## Cấu trúc

| Đường dẫn | Trang | Nội dung chính |
|---|---|---|
| `/` | Trang chủ | Định vị, 5 lối vào theo nhu cầu, 4 công cụ, 5 trụ cột, dự án, tri thức, mạng lưới, form báo giá |
| `/dich-vu/` | Dịch vụ | 5 trụ cột chi tiết, trình tự thực hiện kiểm toán quyết toán 5 bước |
| `/cong-cu/` | Công cụ | **Máy tính phí kiểm toán + thẩm tra quyết toán**, bảng định mức, hỏi đáp |
| `/du-an/` | Dự án | 9 công trình tiêu biểu, lọc theo lĩnh vực |
| `/tri-thuc/` | Tri thức | Bài viết lọc theo chủ đề, **thư viện văn bản còn/hết hiệu lực** |
| `/ve-asco/` | Về ASCO | Năng lực bằng số, chứng nhận, minh bạch, mạng lưới 11 điểm |
| `/tuyen-dung/` | Tuyển dụng | 4 nhóm vị trí, lộ trình nghề nghiệp |

## Máy tính phí

Cài đặt tại `cong-cu/index.html`. Định mức theo **Điều 20 Nghị định 193/2026/NĐ-CP**:

| Tổng mức đầu tư | Phí kiểm toán | Phí thẩm tra |
|---|---|---|
| ≤ 5 tỷ | 0,96 % | 0,57 % |
| 10 tỷ | 0,645 % | 0,39 % |
| 50 tỷ | 0,45 % | 0,285 % |
| 100 tỷ | 0,345 % | 0,225 % |
| 500 tỷ | 0,195 % | 0,135 % |
| 1.000 tỷ | 0,129 % | 0,09 % |
| ≥ 10.000 tỷ | 0,069 % | 0,048 % |

Giá trị giữa hai mốc được **nội suy tuyến tính** — đây là chỗ nhiều nơi tính sai do làm tròn lên mốc trên.
Tối thiểu: 1 triệu đồng (kiểm toán, chưa thuế) và 0,5 triệu đồng (thẩm tra, không thuế).
Dự án đã kiểm toán độc lập được giảm 50% phí thẩm tra.

> **Cần đối chiếu:** bảng tỷ lệ trên cần ASCO xác nhận lại với bản ký của Điều 20 Nghị định 193/2026
> trước khi công bố chính thức.

## Việc còn phải làm

- [ ] Kích hoạt FormSubmit: lần đầu có người gửi form, thư kích hoạt về `asco@asco.vn`, bấm "Activate Form" một lần
- [ ] Điền mã đo lường Google Analytics 4
- [ ] Chép nội dung nhận xét khách hàng từ asco.vn hiện tại (3 ô đang để trống, không tự bịa)
- [ ] Bổ sung trang đội ngũ: họ tên, chức danh, số chứng chỉ hành nghề, ảnh
- [ ] Bổ sung 3–5 dự án nông nghiệp &amp; thuỷ lợi tiêu biểu
- [ ] Bổ sung biểu phí thẩm định giá và biểu phí kiểm toán BCTC để hoàn thiện 2 công cụ còn lại
- [ ] Viết nội dung đầy đủ cho các bài trong mục Tri thức
- [ ] Chốt slogan (5 phương án trong báo cáo khảo sát)

## Dựng lại

Site được sinh ra từ các file nguồn rời bằng `build_site.py`. Nếu chỉ sửa nội dung,
sửa thẳng file `index.html` trong từng thư mục là được.
