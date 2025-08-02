# AI-Driven Interview Workflow

## 🚀 Overview

This repository contains an automated AI-powered interview workflow built using **n8n**, **Redis**, **Google Sheets**, and **Google Gemini**. The system dynamically generates endless interview questions, captures user responses, and stores them systematically for analysis. Ideal for automating initial candidate screening or research interviews.

## 🎯 Features

* **Dynamic AI Interviewer**: Automatically generates interview questions based on the interaction.
* **Persistent Session Management**: Uses Redis for fast, scalable session storage.
* **Real-Time Response Capture**: Records user responses and timestamps systematically.
* **Data Analysis Integration**: Captures all responses in Google Sheets for further review.
* **User-Friendly Interface**: Simple form-based interactions.
* **Transcript Generation**: Users receive a full transcript of their interaction upon completion.

## 🛠️ Technology Stack

* [n8n](https://n8n.io/) – Workflow automation tool
* [Redis](https://redis.io/) via [Upstash](https://upstash.com/) – Session and data storage
* [Google Sheets](https://docs.google.com/spreadsheets/) – Data analysis and storage
* [Google Gemini](https://deepmind.google/gemini/) – AI question generation

## 🌐 Workflow Details

### 1. **Start Interview**

* Initiate via a simple form prompting the user’s name.

### 2. **Dynamic AI Researcher**

* AI continuously generates open-ended questions, adjusting dynamically based on user responses.

### 3. **Response Recording**

* Each user response is captured and stored in Redis with timestamp metadata.

### 4. **Session Management**

* Sessions are created and stored with unique IDs, ensuring each interview is independently managed.

### 5. **Session Transcript**

* On completion, users can view a complete transcript. Sessions automatically expire after 24 hours.

### 6. **Data Integration**

* Interview data is automatically uploaded to Google Sheets, facilitating team analysis.

## 📖 How It Works

* User initiates the interview via the form.
* A unique session is created in Redis.
* The AI interviewer dynamically generates questions.
* Responses are captured and appended to the Redis session.
* Users can stop the interview by typing `STOP`.
* Upon stopping, data is written to Google Sheets, and users receive their interview transcript.

## 📌 Getting Started

### Prerequisites

* n8n installation
* Redis database setup (e.g., via Upstash)
* Google Sheets API credentials
* Google Gemini API credentials

### Installation Steps

1. Clone this repository:

```bash
git clone https://github.com/Devesh-Ingale/AI-Interviewer.git
```

2. Configure your Redis, Google Sheets, and Gemini API credentials in n8n.
3. Import the workflow JSON provided (`INTERVIWER.json`) into n8n.
4. Deploy and run the workflow in your environment.

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to open an issue or pull request.


Distributed under the MIT License.
