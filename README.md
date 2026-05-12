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
| `Models` | Shared response/request models |

---

## 🛠 Tech Stack

- **Backend:** ASP.NET Core Web API
- **Documentation:** Scalar (OpenAPI 3.1)
- **Authentication:** JWT Bearer Tokens + OTP via Email + Google OAuth2
- **AI / ML:** Speech-to-text transcription model
- **Testing:** Postman + Newman (automated HTML reports)
- **Deployment:** runasp.net

---

## 🚀 Getting Started

### Prerequisites

- .NET 8 SDK
- SQL Server / PostgreSQL
- Postman (for manual testing)
- Newman (for automated test runs)

### Installation

```bash
# Clone the repository
git clone https://github.com/eslamwaled150/silent-voice-api.git
cd silent-voice-api

# Restore dependencies
dotnet restore

# Apply database migrations
dotnet ef database update

# Run the API
dotnet run
```

The API will be available at `http://localhost:5000`

---

