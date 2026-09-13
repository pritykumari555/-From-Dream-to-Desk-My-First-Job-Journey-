# 🚀 Day 02 — Backend Basics: Express, Multer & MongoDB

Today I went deep into the **why** behind the backend tools I've been using —
not just how to write the code, but how to explain it in an interview.

## 🎯 What I'm Learning

- Why we use **Express.js** for building servers and REST APIs
- How **HTTP requests** connect the frontend and backend
- What **middleware** actually does, and why `express.json()` matters
- Why **CORS** is needed when frontend and backend run on different origins
- How **Multer** handles file uploads (`memoryStorage`, `upload.single()`)
- Where images *actually* get stored vs. what MongoDB stores
- Why we use a **Mongoose Model** instead of writing raw MongoDB queries
- The difference between `req.body` and `req.params`
- When to use `POST` vs `GET` vs `PUT` vs `PATCH` vs `DELETE`
- Why `async/await` matters for database calls
- Why secrets and config values belong in `.env`, not in code

## 🧠 My Project Flow (Image Upload Feature)

```
Frontend (React)
   ↓ selects image + caption
Multer (memoryStorage)
   ↓ reads file into memory buffer
Storage Service
   ↓ returns image URL
MongoDB (via Mongoose)
   ↓ stores { imageUrl, caption }
Response
   ↓
Frontend renders the new post
```

## 💬 Interview-Ready Answer

> "The uploaded image is sent to a storage service, and after a successful
> upload I get its URL. I store that URL in MongoDB along with the post data —
> I don't need to store the actual image in the database."

## 📌 Key Takeaways

| Concept | One-liner |
|---|---|
| Express | Server + Routes + Middleware + API |
| Middleware | Runs *between* request and response |
| Multer | Middleware for handling file uploads |
| Mongoose | Schema → structure, Model → database operations |
| `.env` | Keeps secrets and config out of source code |

---

📎 Full write-up with all 15 Q&As and code examples: see [`Backend_Interview_Prep.pdf`](./Backend_Interview_Prep.pdf) in this folder.

⬅️ [Back to Day 01](../Day-01/README.md)
