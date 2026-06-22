# Bài 4: Phân tích & Lựa chọn (Iterative Prompting + Tối ưu thuật toán)

---

## 1. Đáp án lựa chọn

**Chọn: B**

---

## 2. Lý do lựa chọn phương án B (theo tiêu chí kỹ thuật)

Phương án B là tối ưu nhất vì nó:

### 1. Xác định rõ vấn đề thuật toán
- Nêu chính xác:
    - Thuật toán hiện tại có độ phức tạp **O(2^N)** (exponential)
    - Gây treo hệ thống khi n = 50

➡️ AI không còn phải “đoán lỗi”, mà hiểu rõ vấn đề hiệu năng.

---

### 2. Chỉ định hướng tối ưu cụ thể
- Yêu cầu rõ:
    - Sử dụng **Dynamic Programming**
    - Có thể chọn:
        - Tabulation (bottom-up)
        - Memoization (top-down)

➡️ Đây là chỉ dẫn thuật toán cụ thể, không mơ hồ.

---

### 3. Ràng buộc hiệu năng rõ ràng
- Time complexity: **O(N)**
- Space complexity: **O(1) hoặc O(N)**

➡️ Đây là yếu tố quan trọng trong tối ưu thuật toán thực tế.

---

### 4. Giữ nguyên hợp đồng hàm (API contract)
- Không thay đổi kiểu trả về `long`

➡️ Đảm bảo tương thích hệ thống hiện tại.

---

## 3. Vì sao phương án B tốt hơn trong Iterative Prompting

- Có phản hồi dựa trên quan sát lỗi (slow / hang)
- Có phân tích nguyên nhân (exponential complexity)
- Có mục tiêu cải tiến rõ ràng
- Có constraint kỹ thuật cụ thể

➡️ Đây là một prompt dạng **debug → refine → optimize loop**

---

## 4. Phân tích các phương án còn lại

---

### ❌ Phương án A
> "Code chạy chậm quá, viết lại bằng thuật toán khác tối ưu hơn"

#### Nhược điểm:
- Không nêu rõ:
    - độ phức tạp hiện tại
    - mục tiêu tối ưu cụ thể
- Không chỉ định kỹ thuật (DP, memoization, v.v.)

➡️ AI có thể:
- viết lại không đúng hướng
- vẫn dùng recursion nhưng “tối ưu giả”

---

### ❌ Phương án C
> "Dùng Java Stream API và parallel"

#### Nhược điểm:
- Sai bản chất bài toán:
    - Fibonacci là bài toán phụ thuộc trạng thái (state-dependent)
    - Không phù hợp parallel stream
- Có nguy cơ:
    - overhead thread lớn hơn lợi ích
    - kết quả không tối ưu hoặc sai thiết kế

➡️ Đây là **over-engineering + misuse of parallelism**

---

## 5. Kết luận

- **Phương án đúng: B**
- Vì đảm bảo:
    - đúng phân tích thuật toán
    - đúng hướng tối ưu (DP)
    - có ràng buộc complexity rõ ràng
    - phù hợp iterative prompting

---