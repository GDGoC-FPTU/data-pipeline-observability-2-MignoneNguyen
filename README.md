[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=24112878&assignment_repo_type=AssignmentRepo)
# Day 10 Lab: Data Pipeline & Data Observability

**Student Email:** ducksfromandromeda@gmail.com
**Name:** Nguyen Minh Anh

---

## Mô tả

Bài lab này hướng dẫn cách xây dựng một quy trình ETL (Extract, Transform, Load) tự động cơ bản bằng Python và Pandas. Các công việc cụ thể đã thực hiện:
- **Extract**: Đọc dữ liệu đầu vào từ file định dạng JSON (`raw_data.json`).
- **Validate**: Kiểm tra và loại bỏ các dữ liệu không hợp lệ (ví dụ: sản phẩm có giá <= 0, danh mục bị bỏ trống).
- **Transform**: Xử lý và làm sạch dữ liệu bằng cách tính toán giá sau khi giảm giá 10% (`discounted_price`), chuẩn hóa tên danh mục thành dạng chữ hoa đầu từ (Title Case) và thêm trường thời gian xử lý (`processed_at`).
- **Load**: Lưu kết quả dữ liệu đã được làm sạch và biến đổi ra file định dạng CSV (`processed_data.csv`).
- **Agent Simulation**: Sau đó dùng output thu được để mô phỏng sự ảnh hưởng của chất lượng dữ liệu (Clean Data vs Garbage Data) tới kết quả phân tích và trả lời của một ứng dụng Agent.

---

## Cach chay (How to Run)

### Prerequisites
```bash
pip install pandas
```

### Chay ETL Pipeline
```bash
python solution.py
```

### Chay Agent Simulation (Stress Test)
```bash
python agent_simulation.py
```

---

## Cau truc thu muc

```
├── solution.py              # ETL Pipeline script
├── processed_data.csv       # Output cua pipeline
├── experiment_report.md     # Bao cao thi nghiem
└── README.md                # File nay
```

---

## Kết quả

- **Tổng số records đầu vào:** 5
- **Số records hợp lệ (Valid):** 3
- **Số records bị loại (Dropped):** 2 (Các lỗi: 'Price <= 0', 'Category is empty')
- Dữ liệu cuối cùng được biến đổi và lưu thành công vào file `processed_data.csv`.
