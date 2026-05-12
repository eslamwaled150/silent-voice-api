# 🤝 Silent Voice API

> A RESTful API that bridges the communication gap for people with hearing and speech impairments — converting sign language gestures and voice audio into accessible digital content.

---

## 📖 About the Project

**Silent Voice** is a graduation project API built to assist individuals who are deaf, hard of hearing, or speech-impaired. The system provides:

- 🤟 **Sign Language Recognition** — Save and retrieve sign language gesture data
- 🎙️ **Voice Transcription** — Upload audio files and receive text transcriptions
- 🔐 **Secure Authentication** — Full auth flow with JWT + email OTP verification and password reset
- 🌐 **Google Login** — OAuth2 social authentication support

---

## 📄 API Documentation

Interactive API docs powered by **Scalar (OpenAPI 3.1)**:

🔗 **[silentvoice.runasp.net/scalar](http://silentvoice.runasp.net/scalar/)**

> Download the OpenAPI spec directly from the docs page (JSON or YAML format).

---

## 🧩 API Modules

| Module | Description |
|--------|-------------|
| `Auth` | Register, login, email OTP confirmation, Google login, forgot/reset password |
| `Sign` | Save sign language data, view history, delete records |
| `Voice` | Upload & transcribe audio, manage transcription history, stream audio files |

---

## 🛠 Tech Stack

| Layer | Tool |
|-------|------|
| API | ASP.NET Core Web API |
| Documentation | Scalar (OpenAPI 3.1) |
| Authentication | JWT + OTP via Email + Google OAuth2 |
| AI / ML | Speech-to-text transcription model |
| API Testing | Postman |
| Automated Testing | Newman + HTML Extra Reporter |
| Deployment | runasp.net |

---
## 🧪 Testing with Newman

### Prerequisites

Make sure you have **Node.js** installed, then run:

```bash
npm install -g newman
npm install -g newman-reporter-htmlextra
```

Verify installation:

```bash
newman --version
```

---

### ▶️ Run the Collection

```bash
newman run Silent_Voice_postman_collection.json \
  -e Environment_Silent_Voice_postman_environment.json \
  --reporters cli,htmlextra \
  --reporter-htmlextra-export newman-report.html
```

---

### 📊 View the HTML Report

After the run completes, open the report in your browser:

```bash
# Windows
start newman-report.html

# Mac
open newman-report.html
```

Or simply double-click `newman-report.html` from File Explorer.
