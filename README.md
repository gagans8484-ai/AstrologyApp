# AstrologyApp 🌙

A comprehensive Vedic Astrology Android application that provides complete astrological insights including birth charts, horoscopes, dashas, yogas, nakshatras, and compatibility readings.

## Tech Stack

### Frontend
- **Language:** Kotlin
- **Framework:** Android Jetpack (MVVM Architecture)
- **UI:** Material Design 3
- **HTTP Client:** Retrofit + OkHttp

### Backend
- **Language:** Python 3.9+
- **Framework:** FastAPI
- **Astrology Engine:** Swiss Ephemeris + Vedic Libraries
- **Database:** PostgreSQL
- **Deployment:** Docker

## Features

- 🌍 **Birth Chart Generation** - Calculate natal charts from date/time/location
- 📅 **Daily/Weekly/Monthly Horoscopes** - Personalized predictions
- 🔄 **Dasha Predictions** - Vimshottari dasha calculations
- 🌟 **Nakshatra Information** - Complete nakshatra details
- 💫 **Yoga Calculations** - Planetary yoga combinations
- 💕 **Compatibility Readings** - Synastry and composite charts
- 📊 **Transit Predictions** - Current planetary transits
- 👤 **User Profiles** - Save and manage multiple charts

## Project Structure

```
AstrologyApp/
├── android/                 # Android app (Kotlin)
│   ├── app/
│   │   ├── src/
│   │   │   ├── main/
│   │   │   │   ├── java/com/astrology/
│   │   │   │   │   ├── ui/
│   │   │   │   │   ├── viewmodel/
│   │   │   │   │   ├── repository/
│   │   │   │   │   ├── network/
│   │   │   │   │   └── models/
│   │   │   │   └── res/
│   │   └── build.gradle
│   └── settings.gradle
├── backend/                 # Python backend
│   ├── app/
│   │   ├── main.py
│   │   ├── models/
│   │   ├── api/
│   │   ├── services/
│   │   ├── calculations/
│   │   └── database/
│   ├── requirements.txt
│   ├── Dockerfile
│   └── docker-compose.yml
└── docs/                    # Documentation

```

## Getting Started

### Android Setup
1. Clone the repo
2. Open `android/` in Android Studio
3. Sync Gradle dependencies
4. Configure API endpoint in `BuildConfig`
5. Run on emulator or device

### Backend Setup
1. Install Python 3.9+
2. `pip install -r backend/requirements.txt`
3. Configure PostgreSQL
4. Run: `uvicorn app.main:app --reload`
5. API docs at `http://localhost:8000/docs`

## API Endpoints

- `POST /api/charts` - Generate birth chart
- `GET /api/horoscope/{sign}` - Get daily horoscope
- `GET /api/dasha/{chart_id}` - Get dasha predictions
- `GET /api/compatibility` - Compatibility analysis
- `POST /api/users` - Create user profile
- `GET /api/transits` - Current transits

## Dependencies

### Backend
- swisseph (Swiss Ephemeris)
- fastapi
- sqlalchemy
- pydantic
- psycopg2

### Android
- Jetpack Compose / Material Design
- Retrofit
- Room Database
- Coroutines

## License

MIT License - Feel free to use and modify

## Contributing

Pull requests welcome! Please follow the code style and add tests for new features.

## Roadmap

- [ ] Push notifications for important transits
- [ ] Augmented Reality birth chart visualization
- [ ] Social features (sharing charts)
- [ ] Advanced yoga calculations
- [ ] Remedies and recommendations engine
- [ ] Multiple language support

---

**Made with ❤️ for astrology enthusiasts**
