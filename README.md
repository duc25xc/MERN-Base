# 🚀 MERN-Base

> **Clone. Config. Code.** — Không còn mất hàng giờ setup mỗi khi bắt đầu dự án mới.

---

## 🧩 Vấn đề

Mỗi khi khởi động một dự án MERN mới, bạn phải lặp lại cùng một quy trình:

- Tạo cấu trúc thư mục từ đầu
- Cài đặt và cấu hình Express, Mongoose, CORS, dotenv...
- Setup Vite + React, cấu hình ESLint + Prettier
- Kết nối MongoDB, viết boilerplate server
- Tổ chức lại folders cho đúng pattern MVC + Service Layer
- Mất **1–3 tiếng** chỉ để có thể bắt đầu viết business logic

**MERN-Base giải quyết điều đó.** Clone về, cấu hình `.env`, chạy `npm run dev` — và bạn đã sẵn sàng code thật sự.

---

## ✨ Có gì trong này?

### Backend — Express 5 + MongoDB

- Cấu trúc **MVC + Service Layer** rõ ràng, dễ mở rộng
- **Express 5** với ES Modules (`type: "module"`)
- **Mongoose 9** kết nối MongoDB
- **CORS, dotenv, nodemon** được cấu hình sẵn
- Thư mục `config/`, `middlewares/`, `utils/` cho các logic dùng chung

### Frontend — React 19 + Vite 7

- **Vite 7** — build cực nhanh, HMR mượt mà
- **React 19** với cấu trúc thư mục rõ ràng
- Thư mục `api/`, `hooks/`, `context/`, `layouts/`, `pages/`, `components/`
- **ESLint + Prettier** được cấu hình và tích hợp sẵn

### Developer Experience

- Chạy **cả backend lẫn frontend** chỉ với 1 lệnh từ root
- `.env.example` để team biết cần config gì
- `docs/` với hướng dẫn setup, tips và danh sách thư viện gợi ý

---

## 📁 Cấu trúc thư mục

```
mern-base/
├── backend/
│   └── src/
│       ├── config/          # Kết nối DB, biến môi trường
│       ├── controllers/     # Xử lý request/response
│       ├── middlewares/     # Auth, error handler, ...
│       ├── models/          # Mongoose schemas
│       ├── routes/          # Định nghĩa API routes
│       ├── services/        # Business logic
│       ├── utils/           # Helper functions
│       └── server.js        # Entry point
├── frontend/
│   └── src/
│       ├── api/             # Gọi API (axios/fetch)
│       ├── assets/          # Hình ảnh, fonts, ...
│       ├── components/      # UI components tái sử dụng
│       ├── context/         # React Context / global state
│       ├── hooks/           # Custom hooks
│       ├── layouts/         # Layout wrappers
│       ├── pages/           # Page components (route-level)
│       ├── utils/           # Helper functions
│       └── main.jsx         # Entry point
├── docs/
│   ├── setup.md             # Hướng dẫn setup chi tiết
│   ├── libraries.md         # Thư viện gợi ý theo từng use case
│   └── tips.md              # Tips & tricks
└── package.json             # Root — chạy cả 2 cùng lúc
```

---

## ⚡ Bắt đầu nhanh

### 1. Clone repo

```bash
git clone https://github.com/duc25xc/MERN-Base.git my-project
cd my-project
```

### 2. Cài dependencies

```bash
# Cài concurrently ở root
npm install

# Cài dependencies cho backend
cd backend && npm install

# Cài dependencies cho frontend
cd ../frontend && npm install
```

### 3. Cấu hình môi trường

```bash
# Tạo file .env từ template
cp backend/.env.example backend/.env
```

Mở `backend/.env` và điền thông tin:

```env
PORT=5000
MONGO_URI=mongodb://localhost:27017/your_db_name
NODE_ENV=development
```

### 4. Chạy project

```bash
# Từ thư mục root — chạy cả backend & frontend cùng lúc
npm run dev
```

| Service  | URL                   |
| -------- | --------------------- |
| Backend  | http://localhost:5000 |
| Frontend | http://localhost:5173 |

---

## 🛠️ Scripts

| Lệnh             | Mô tả                      |
| ---------------- | -------------------------- |
| `npm run dev`    | Chạy cả backend + frontend |
| `npm run dev:be` | Chỉ chạy backend           |
| `npm run dev:fe` | Chỉ chạy frontend          |

---

## 📦 Tech Stack

| Layer     | Technology                |
| --------- | ------------------------- |
| Frontend  | React 19, Vite 7          |
| Backend   | Node.js, Express 5        |
| Database  | MongoDB, Mongoose 9       |
| Dev Tools | ESLint, Prettier, Nodemon |

---

## 📋 Yêu cầu

- **Node.js** >= 18.x
- **npm** >= 9.x
- **MongoDB** (local hoặc MongoDB Atlas)

---

## 📖 Tài liệu

| File                | Nội dung                           |
| ------------------- | ---------------------------------- |
| `docs/setup.md`     | Hướng dẫn setup chi tiết từng bước |
| `docs/libraries.md` | Gợi ý thư viện theo từng use case  |
| `docs/tips.md`      | Tips khi phát triển với stack này  |

---

## 🔧 Tuỳ chỉnh cho dự án mới

Khi fork/clone repo này cho một dự án mới:

1. Đổi `name` trong `backend/package.json` và `frontend/package.json`
2. Cập nhật `MONGO_URI` trong `.env`
3. Xoá hoặc thay thế nội dung trong `src/routes/`, `src/models/` bằng logic của dự án
4. Bắt đầu code 🎉

---

## 📄 License

MIT — Dùng thoải mái, fork thoải mái.
