# 📊 BÁO CÁO THU HOẠCH NGHIỆM THU BÀI LAB 3 (BƯỚC 3 — SUBMISSION ARTIFACT)

> **Họ và Tên Học viên:** Vũ Minh Trí
> **Mã Sinh Viên / Mã Học viên:** 2A202602629
> **Chủ đề Lựa chọn:** Trợ lý Học vụ & Tra cứu Lịch thi VinUni: Tra cứu điểm GPA, lịch thi và đặt lịch tư vấn học vụ với Cố vấn.

---

## 1. BẢNG CHẤM ĐIỂM AGENTIC FIT SCORING MATRIX (ĐÁNH GIÁ CHỦ ĐỀ)

| Tiêu chí Đánh giá           | Mức độ (1 - 5) | Giải trình chi tiết lý do chọn điểm                                                                                                                                                                                                                                                                         |
| :-------------------------- | :------------: | :---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **1. Multi-step Reasoning** |      4/ 5      | Một yêu cầu có thể cần nhiều bước. Ví dụ: “GPA hiện tại của tôi bao nhiêu và tôi có lịch thi nào tuần tới?” → xác định sinh viên → lấy dữ liệu GPA → lấy lịch thi → lọc theo thời gian → tổng hợp câu trả lời. Nếu đặt lịch cố vấn thì còn thêm bước kiểm tra lịch trống → chọn slot → xác nhận → đặt lịch. |
| **2. Tool Interaction**     |      5/ 5      | Hệ thống cần tương tác với nhiều nguồn/tool bên ngoài: Student Information System/Database, Exam Schedule, Calendar/Appointment System. Agent không tự biết GPA hay lịch thi thực tế mà phải gọi tool để lấy dữ liệu.                                                                                       |
| **3. Dynamic Decision**     |     4 / 5      | Bước tiếp theo có thể phụ thuộc vào kết quả trước. Ví dụ: kiểm tra lịch cố vấn → nếu slot mong muốn hết → tìm slot khác → nếu người dùng xác nhận → mới thực hiện booking                                                                                                                                   |
| **4. Long Horizon Goal**    |      3/ 5      | Có thể duy trì mục tiêu qua nhiều bước khi thực hiện một workflow như “tìm lịch trống và đặt lịch với cố vấn”. Nhưng phần lớn tác vụ chỉ cần vài bước và kết thúc nhanh, không phải một mục tiêu dài hạn phức tạp.                                                                                          |
| **TỔNG ĐIỂM AGENTIC FIT**   |   **16/ 20**   | _Nếu tổng điểm > 12/20: Bài toán rất phù hợp triển khai Agentic System._                                                                                                                                                                                                                                    |

---

## 2. TRÍCH XUẤT KẾT QUẢ WATERFALL TRACE LOG (SAU KHI CHẠY TEST SUITE TRÊN API THẬT)

> ⚠️ **YÊU CẦU NGHIỆM THU:** Mở tệp `.env` điền `GEMINI_API_KEY` (hoặc `OPENAI_API_KEY`) để kết nối LLM thật trước khi thực thi `python src/app.py --all`. Bài nộp chỉ dùng Mock Offline Provider sẽ không đạt điểm nghiệm thực tế.

Dán 1 đoạn trích xuất log tiêu biểu từ file `docs/trace_waterfall.json` sinh ra từ phản hồi LLM API thật:

```json
[
  {
    "step": 1,
    "action_type": "TOOL_EXECUTION",
    "tool_name": "academic_query",
    "arguments": {
      "student_id": "SV2026001"
    },
    "observation": {
      "status": "SUCCESS",
      "student_id": "SV2026001",
      "data": {
        "full_name": "Nguyễn Văn An",
        "gpa": 3.85
      }
    },
    "latency_ms": 120.5
  }
]
```

---

## 3. TỔNG KẾT KẾT QUẢ NGHIỆM THU & NỘP BÀI

- [ ] Đã điền API Key thật trong `.env` và xác nhận Agent chạy mượt mà trên LLM API thật (Gemini/OpenAI).
- **Tổng số Test Cases đã chạy thành công:** \_\_\_ / 5 test cases.
- **Số lượt gọi Tool qua MCP Server chính xác:** \_\_\_ lượt.
- **Kết quả đẩy Repo nộp bài:** [ ] Đã Commit và Push mã nguồn thành công lên GitHub cá nhân.

---

> ✅ **HOÀN TẤT NỘP BÀI:** Sao chép đường link GitHub Repository cá nhân của bạn và dán vào ô nộp bài trên hệ thống LMS VLearn để hoàn tất Bài Lab 3!
