# Anime Recommendation App

An Android anime recommendation application integrated with the Jikan API and a Java Servlet backend. The system allows users to select anime genres and minimum scores, then returns a random anime recommendation with its title, image, and synopsis.

---

## Features

### Android Application
- Genre selection using `Spinner`
- Minimum score input using `EditText`
- Anime poster display with `ImageView`
- Background threading for network requests
- JSON parsing and UI updates
- Glide library integration for asynchronous image loading
- User-friendly error handling with Toast messages

### Web Service
- Java Servlet middleware between Android client and Jikan API
- RESTful API implementation
- Data minimization to reduce bandwidth usage
- Dynamic anime filtering by genre and score

### Database & Logging
- MongoDB Atlas cloud database integration
- Logs request metadata including:
  - Timestamp
  - Device information
  - Client IP address
  - Genre selection
  - API status code
  - Processing latency

### Dashboard & Analytics
- Web dashboard for monitoring operations
- Analytics including:
  - Total traffic
  - Average response latency
  - Most popular genre
- Clean HTML log table rendering

### Deployment
- Fully deployed using GitHub Codespaces
- Docker container support
- Public API endpoint access

---

# Tech Stack

## Frontend
- Android Studio
- Java
- XML Layouts
- Glide Library

## Backend
- Java Servlet
- REST API
- HttpURLConnection

## Database
- MongoDB Atlas

## Deployment
- GitHub Codespaces
- Docker

## Third-Party API
- Jikan API v4
- MyAnimeList anime data

---

# API Information

## Jikan API Endpoint
```text
https://api.jikan.moe/v4/anime
```

## Web Service Endpoint
```text
https://didactic-capybara-94x97q5jj96c79vq-8080.app.github.dev/getAnime
```

---

# Application Workflow

1. User selects:
   - Anime genre
   - Minimum score

2. Android app sends a request to the Java Servlet backend

3. Backend fetches anime data from the Jikan API

4. Server filters and minimizes returned data

5. Android app displays:
   - Anime title
   - Anime image
   - Anime synopsis

---

# Example Backend Logic

```java
String searchUrl =
    "https://api.jikan.moe/v4/anime?genres="
    + genreId
    + "&min_score="
    + minScore
    + "&order_by=score&sort=desc";
```

---

# Error Handling

The application includes:
- Input validation
- Network exception handling
- JSON parsing protection
- User-friendly error messages
- Graceful fallback behavior

---

# Dashboard URL

```text
https://didactic-capybara-94x97q5jj96c79vq-8080.app.github.dev/
```

---

# MongoDB Logging Example

```json
{
  "timestamp": "...",
  "deviceInfo": "...",
  "remoteAddress": "...",
  "genreSelected": "...",
  "httpStatus": 200,
  "processingLatency": 850
}
```


