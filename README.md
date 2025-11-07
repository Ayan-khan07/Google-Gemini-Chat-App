# Google-Gemini-Chat-App
🤖 A Java Spring Boot backend service that provides a REST API interface for the Google Gemini AI.
# Gemini AI Chat Application

A simple backend REST API built with Java and Spring Boot that connects to the Google Gemini AI. This project allows you to send questions to a secure endpoint and receive answers directly from the Gemini model.

This project was built to demonstrate the use of Spring Boot's `WebClient` for integrating with external AI services and securely managing API credentials.

## 🚀 Key Features

* **RESTful Endpoint:** Provides a simple `/api/qna/ask` endpoint for all Q&A requests.
* **Gemini AI Integration:** Connects directly to the Google Gemini AI API to stream responses.
* **Asynchronous API Calls:** Uses Spring `WebClient` for efficient, non-blocking HTTP requests to the external API.
* **Secure Configuration:** Securely manages the Google API key and URL using environment variables, which are injected at runtime with Spring's `@Value` annotation.

## 🛠️ Technologies Used

* **Java 21**
* **Spring Boot 3**
* **Spring MVC:** For creating the REST controller.
* **Spring WebClient:** For making asynchronous web requests.
* **Maven:** For project dependencies and build management.

## 🏁 How to Run

1.  **Clone the repository:**
    ```sh
    git clone [your-repo-url]
    cd chatApp
    ```

2.  **Set Environment Variables:**
    This project will **not** run without setting the following environment variables. In IntelliJ IDEA, you can do this in **Run > Edit Configurations... > Environment variables**.

    * **Name:** `GEMINI_API_URL`
    * **Value:** `https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent`

    * **Name:** `GEMINI_API_KEY`
    * **Value:** `YOUR_OWN_GOOGLE_AI_KEY` (Get this from Google AI Studio)

3.  **Run the application:**
    You can either run the main `ChatAppApplication` class in your IDE or use Maven:
    ```sh
    mvn spring-boot:run
    ```

## 🧪 API Usage

You can test the endpoint using Postman or any API client.

* **URL:** `http://localhost:8080/api/qna/ask`
* **Method:** `POST`
* **Body (JSON):**
    ```json
    {
      "question": "How does Spring Boot WebClient work?"
    }
    ```

The server will respond with the JSON answer from the Gemini AI.
