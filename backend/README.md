# **FastAPI Backend with JWT Authentication & Virtual Wallet**
*A backend task for those applying for TQ Tech Department*

## ** Core Requirements (Mandatory)**
Build a FastAPI backend with:
1. **User Authentication**:
   - Register/login with JWT tokens.
   - Password hashing.
2. **Virtual Wallet**:
   - Users start with **₹100** (hardcoded or seeded).
   - Endpoints to:
     - View balance (`GET /wallet/balance`).
     - Spend money (`POST /wallet/spend`).
3. **Items System**:
   - Pre-populate the database with **3-5 items** (e.g., "Book: ₹50").
   - Users can buy items (`POST /items/buy/{item_id}`).
4. **Database**:
   - Store users, items, and transactions (schema below).
5. **README**:
   - Setup instructions, API examples

---

## ** Brownie Points (Optional)**
Enhance the project with **admin features** (not mandatory but encouraged):
1. **Role-Based Access**:
   - Add an `admin` role (default: `user`).
   - Admins can:
     - Add items (`POST /admin/items`).
     - Credit user wallets (`POST /admin/wallet/credit`).
2. **Extras**:
   - Transaction history (`GET /wallet/transactions`).
   - Dockerize the app.
   - Input validation (e.g., prevent negative spending).

---

## **🗃 Database Schema**



| Table          | Fields (Key: Type)                                                                 | Notes                                  |
|----------------|------------------------------------------------------------------------------------|----------------------------------------|
| `users`        | `id`: UUID (PK), `username`: str (unique), `password_hash`: str, `wallet_balance`: int | Default `wallet_balance`: 100.         |
| `items`        | `id`: UUID (PK), `name`: str, `price`: int, `stock`: int                           | Pre-populate with 3-5 items.           |
| `transactions` | `id`: UUID (PK), `user_id`: UUID (FK), `item_id`: UUID (FK), `amount`: int, `timestamp`: datetime | Logs purchases.                        |



| Table          | Additional Fields/Notes (brownie points)                                               |
|----------------|----------------------------------------------------------------------------------------|
| `users`        | `role`: str ("user" or "admin")                                                        |
| `transactions` | `type`: str ("purchase" or "credit") to distinguish admin-top-ups from user spending. |

---

## ** Setup Instructions**
- Any Framework is fine
- **Database**: Use [Neon](https://neon.tech/) (PostgreSQL) or [MongoDB Atlas](https://www.mongodb.com/atlas/database) or Supabase or if you are feeling fancy Postgres or any SQL DB Dockerized / locally
- **API Testing**: [Postman](https://www.postman.com/) or [Bruno](https://www.usebruno.com/) or good old curl

---

## ** API Endpoints**
### **Core (Mandatory)**
| Endpoint               | Method | Description                          | Example Request Body               |
|------------------------|--------|--------------------------------------|------------------------------------|
| `/auth/register`       | POST   | Register a new user.                | `{"username": "alice", "password": "secret"}` |
| `/auth/login`          | POST   | Login and get JWT.                   | `{"username": "alice", "password": "secret"}` |
| `/wallet/balance`      | GET    | View current balance.               | (JWT in `Authorization` header)    |
| `/wallet/spend`        | POST   | Deduct amount from wallet.          | `{"amount": 30}`                   |
| `/items`               | GET    | List all items.                     |                                    |
| `/items/buy/{item_id}` | POST   | Buy an item (deducts price).        |                                    |

### **Brownie Points (Optional)**
| Endpoint               | Method | Description                          | Example Request Body               |
|------------------------|--------|--------------------------------------|------------------------------------|
| `/admin/items`         | POST   | Add a new item (admin-only).         | `{"name": "Pen", "price": 10, "stock": 50}` |
| `/admin/wallet/credit` | POST   | Credit a user’s wallet (admin-only).| `{"user_id": "UUID", "amount": 50}` |

---

## ** Testing**
### **Sample `curl` Commands**
*Do note to change the localhost port to the port you are running the server on*
1. **Register a User**:
   ```bash
   curl -X POST "http://localhost:8000/auth/register" -H "Content-Type: application/json" -d '{"username":"bob","password":"bob123"}'
   ```
2. **Login**:
   ```bash
   curl -X POST "http://localhost:8000/auth/login" -H "Content-Type: application/json" -d '{"username":"bob","password":"bob123"}'
   ```
   → Save the returned `access_token` for authenticated routes.
3. **Spend Money**:
   ```bash
   curl -X POST "http://localhost:8000/wallet/spend" -H "Authorization: Bearer YOUR_JWT" -H "Content-Type: application/json" -d '{"amount":20}'
   ```


## ** Resources**
| Tool               | Purpose                          | Link                                  |
|--------------------|----------------------------------|---------------------------------------|
| **Neon**          | Free PostgreSQL database.        | [neon.tech](https://neon.tech/)      |
| **Postman**       | API testing.                     | [postman.com](https://www.postman.com/) |
| **Bruno**         | Lightweight Postman alternative. | [usebruno.com](https://www.usebruno.com/) |
| **FastAPI Docs**   | Making API's using Python.              | [fastapi.tiangolo.com](https://fastapi.tiangolo.com/) |
| **Express JS**    | API testing.                     | [expressjs.com](https://expressjs.com/) |
---

## ** Evaluation Criteria**
| Criteria          | Weight | Notes                                                                 |
|-------------------|--------|-----------------------------------------------------------------------|
| **Core Features** | 70%    | Auth, wallet, items, and transactions work correctly.                |
| **Code Quality**  | 20%    | Modular, clean, and well-commented.                                  |
| **Documentation** | 10%    | README is clear with setup/testing steps.                            |
| **Brownie Points**| Bonus  | Admin routes, Docker, or transaction history.                        |