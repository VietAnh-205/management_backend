# 🛍️ Store Management System (RS Management)



## 📝 Giới thiệu
**RS Management** là một hệ thống quản lý cửa hàng toàn diện, được thiết kế để giải quyết bài toán vận hành từ khâu nhập kho, quản lý lô hàng (Batch) đến tối ưu hóa quy trình bán hàng (POS). 

Đặc biệt, hệ thống tích hợp module **Dự báo doanh thu (Sales Forecasting)** dựa trên dữ liệu lịch sử, giúp chủ cửa hàng đưa ra các quyết định nhập hàng thông minh hơn.

---

## 🚀 Tính Năng Cốt Lõi

| Tính năng | Mô tả chi tiết kỹ thuật | Trạng thái |
|:--- |:--- |:---:|
| **📦 Quản Lý Kho** | Kiểm soát Batch-based Stock, Inventory Adjustment và chuyển kho (Transfer). | ✅ Hoàn thành |
| **💵 Bán Hàng (POS)** | Xử lý Sale Order, tính toán Voucher, hỗ trợ Sale Return và in hóa đơn. | ✅ Hoàn thành |
| **📈 Dự Báo Doanh Thu** | Tích hợp công cụ dự báo (Forecasting Engine) sử dụng các mô hình Time Series. | 🧪 Thử nghiệm |
| **🔐 Bảo Mật & Quyền** | Phân quyền dựa trên vai trò (RBAC) với hệ thống Permission Aspect linh hoạt. | ✅ Hoàn thành |
| **👥 Quản Lý Đối Tác** | Theo dõi thông tin Khách hàng, Nhà cung cấp (Supplier) và lịch sử giao dịch. | ✅ Hoàn thành |

---

## 🛠 Tech Stack

Hệ thống được xây dựng trên kiến trúc hiện đại, đảm bảo tính ổn định và khả năng mở rộng cao.

### Backend & AI
<p align="left">
  <img src="https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" />
  <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi" />
  <img src="https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white" />
  <img src="https://img.shields.io/badge/JWT-black?style=for-the-badge&logo=JSON%20web%20tokens" />
</p>

### Frontend & UI
<p align="left">
  <img src="https://img.shields.io/badge/react-%2320232a.svg?style=for-the-badge&logo=react&logoColor=%2361dafb" />
  <img src="https://img.shields.io/badge/tailwindcss-%2338B2AC.svg?style=for-the-badge&logo=tailwind-css&logoColor=white" />
  <img src="https://img.shields.io/badge/Ant_Design-0170FE?style=for-the-badge&logo=ant-design&logoColor=white" />
</p>

### Infrastructure & Tools
<p align="left">
  <img src="https://img.shields.io/badge/docker-%230db7ed.svg?style=for-the-badge&logo=docker&logoColor=white" />
  <img src="https://img.shields.io/badge/git-%23F05032.svg?style=for-the-badge&logo=git&logoColor=white" />
  <img src="https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white" />
</p>

---

## 📊 Module Dự Báo (Forecasting Module)
Đây là điểm nhấn kỹ thuật của dự án. Hệ thống sử dụng một Service riêng biệt được xây dựng bằng **FastAPI** để:
*   Phân tích dữ liệu bán hàng lịch sử từ DB MySQL.
*   Áp dụng các thuật toán như **Exponential Smoothing** hoặc các mô hình nâng cao để dự đoán lượng hàng bán ra trong tuần tiếp theo.
*   Hỗ trợ chủ cửa hàng giảm thiểu tình trạng tồn kho quá mức hoặc thiếu hàng (Out-of-stock).

---



cd forecasting-service
pip install -r requirements.txt
uvicorn main:app --reload
