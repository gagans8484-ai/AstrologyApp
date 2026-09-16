# AstrologyApp - Demo Guide 🌙

This demo shows how the app will work with sample data.

## Demo 1: Birth Chart Generation

### Input:
```json
{
  "name": "John Doe",
  "birth_date": "1990-05-15",
  "birth_time": "14:30:00",
  "birth_location": "New York",
  "latitude": 40.7128,
  "longitude": -74.0060,
  "timezone": "America/New_York"
}
```

### Output (Birth Chart):
```json
{
  "id": 1,
  "name": "John Doe",
  "sun_sign": "Taurus",
  "moon_sign": "Gemini",
  "rising_sign": "Leo",
  "planets": [
    {
      "planet": "Sun",
      "sign": "Taurus",
      "degree": 24.5,
      "house": "2nd"
    },
    {
      "planet": "Moon",
      "sign": "Gemini",
      "degree": 12.3,
      "house": "3rd"
    },
    {
      "planet": "Mercury",
      "sign": "Taurus",
      "degree": 28.7,
      "house": "2nd"
    },
    {
      "planet": "Venus",
      "sign": "Cancer",
      "degree": 15.4,
      "house": "5th"
    },
    {
      "planet": "Mars",
      "sign": "Leo",
      "degree": 8.9,
      "house": "6th"
    },
    {
      "planet": "Jupiter",
      "sign": "Virgo",
      "degree": 5.2,
      "house": "7th"
    },
    {
      "planet": "Saturn",
      "sign": "Capricorn",
      "degree": 18.6,
      "house": "12th"
    }
  ],
  "moon_nakshatra": {
    "name": "Punarvasu",
    "lord": "Jupiter",
    "characteristics": "Renewal, growth, positivity"
  }
}
```

---

## Demo 2: Daily Horoscope

### Request:
```
GET /api/horoscopes/taurus
```

### Response:
```json
{
  "zodiac_sign": "Taurus",
  "date": "2026-09-16",
  "period": "daily",
  "prediction": "Today brings financial opportunities. A conversation with a colleague could lead to new possibilities. Focus on stability and long-term planning.",
  "lucky_number": "6",
  "lucky_color": "Green",
  "mood": "Positive",
  "health_tip": "Take time for physical exercise",
  "love_forecast": "Family relations harmonious"
}
```

---

## Demo 3: Dasha Predictions

### Input:
```
Moon Nakshatra: Punarvasu (Jupiter's Nakshatra)
```

### Output (Current & Upcoming Dashas):
```json
{
  "current_dasha": {
    "lord": "Jupiter",
    "period": "2024-03-15 to 2040-03-15",
    "duration_years": 16,
    "characteristics": "Expansion, growth, wisdom, prosperity",
    "sub_dasha": "Saturn (2026-2029)"
  },
  "upcoming_dashas": [
    {
      "lord": "Saturn",
      "start_date": "2040-03-15",
      "duration_years": 19,
      "characteristics": "Discipline, hard work, karma"
    },
    {
      "lord": "Mercury",
      "start_date": "2059-03-15",
      "duration_years": 17,
      "characteristics": "Communication, intellect, trade"
    }
  ]
}
```

---

## Demo 4: Nakshatra Information

### Request:
```
Moon at 85.5 degrees
```

### Response:
```json
{
  "nakshatra": "Punarvasu",
  "lord": "Jupiter",
  "degree_range": "80 - 93.33",
  "characteristics": [
    "Renewal and growth",
    "Positive outlook",
    "Generosity",
    "Adaptability"
  ],
  "favorable_activities": [
    "New beginnings",
    "Travel",
    "Business ventures",
    "Education"
  ],
  "unfavorable_activities": [
    "Arguments",
    "Destructive work",
    "Major surgery"
  ],
  "lucky_day": "Thursday",
  "lucky_color": "Yellow"
}
```

---

## Demo 5: Compatibility Check

### Request:
```json
{
  "sign1": "Taurus",
  "sign2": "Cancer"
}
```

### Response:
```json
{
  "sign1": "Taurus",
  "sign2": "Cancer",
  "compatibility_score": 85,
  "status": "Highly Compatible",
  "analysis": {
    "emotional_compatibility": 90,
    "communication": 70,
    "trust": 85,
    "values": 88
  },
  "strengths": [
    "Both are nurturing and caring",
    "Strong emotional connection",
    "Shared values around family and home",
    "Natural understanding"
  ],
  "challenges": [
    "Taurus needs stability, Cancer needs reassurance",
    "Different ways of expressing emotions"
  ],
  "advice": "Build strong communication and express feelings openly"
}
```

---

## Demo 6: Current Transits

### Request:
```
GET /api/transits/current
```

### Response:
```json
{
  "date": "2026-09-16",
  "active_transits": [
    {
      "planet": "Mercury",
      "sign": "Libra",
      "date_start": "2026-09-01",
      "date_end": "2026-09-20",
      "impact_level": "medium",
      "description": "Mercury in Libra brings balanced communication. Good time for discussions and negotiations.",
      "affected_signs": ["Gemini", "Virgo", "Libra"]
    },
    {
      "planet": "Venus",
      "sign": "Scorpio",
      "date_start": "2026-09-10",
      "date_end": "2026-10-05",
      "impact_level": "high",
      "description": "Venus in Scorpio intensifies relationships. Deep, passionate connections are highlighted.",
      "affected_signs": ["Scorpio", "Taurus", "Libra"]
    },
    {
      "planet": "Mars",
      "sign": "Gemini",
      "date_start": "2026-08-20",
      "date_end": "2026-10-10",
      "impact_level": "medium",
      "description": "Mars in Gemini brings energetic communication and quick thinking.",
      "affected_signs": ["Aries", "Sagittarius", "Gemini"]
    }
  ]
}
```

---

## Demo 7: User Profile Creation

### Request:
```json
{
  "email": "john@example.com",
  "name": "John Doe"
}
```

### Response:
```json
{
  "id": 1,
  "email": "john@example.com",
  "name": "John Doe",
  "created_at": "2026-09-16T10:30:00",
  "saved_charts": [
    {
      "id": 1,
      "name": "My Birth Chart",
      "sun_sign": "Taurus"
    }
  ]
}
```

---

## Android App Screen Flow

```
┌─────────────────────────────────┐
│   Welcome Screen                │
│  [Register/Login]               │
└──────────┬──────────────────────┘
           │
    ┌──────▼────────┐
    │  Main Menu    │
    ├───────────────┤
    │ 1. Birth Chart│
    │ 2. Horoscope  │
    │ 3. Dasha      │
    │ 4. Nakshatras │
    │ 5. Compatibility│
    │ 6. Transits   │
    │ 7. Profile    │
    └───────────────┘
           │
      ┌────┴─────────────────────┐
      │                          │
   ┌──▼──┐              ┌────────▼────┐
   │Birth│              │ Horoscope   │
   │Chart│              │ (Daily Pred)│
   └─────┘              └─────────────┘
```

---

## API Endpoints Summary

| Endpoint | Method | Purpose |
|----------|--------|---------|
| `/api/charts/generate` | POST | Generate birth chart |
| `/api/charts/{id}` | GET | Get saved birth chart |
| `/api/horoscopes/{sign}` | GET | Get daily horoscope |
| `/api/compatibility/check` | POST | Check zodiac compatibility |
| `/api/transits/current` | GET | Get current planet transits |
| `/api/users/register` | POST | Register new user |
| `/api/users/{id}` | GET | Get user profile |

---

## What Each Feature Does:

### 🌍 Birth Chart
- Shows all planet positions at your birth time
- Calculates your Sun Sign, Moon Sign, Rising Sign
- Determines your Nakshatra (lunar mansion)
- Maps planets to houses

### 📅 Daily Horoscope
- Personalized daily predictions for your zodiac sign
- Lucky numbers and colors
- Health and love forecasts

### 🔄 Dasha Predictions
- Shows major life periods and their rulers
- Current dasha and when it ends
- What to expect during each dasha period

### 🌟 Nakshatras
- 27 lunar mansions explained
- Your moon's nakshatra details
- Favorable and unfavorable activities
- Lucky days and colors

### 💕 Compatibility
- Check romantic compatibility between zodiac signs
- Score from 0-100
- Strengths and challenges in the relationship

### 📊 Transits
- Current planetary positions
- Which signs are affected
- Impact level (high/medium/low)

### 👤 User Profile
- Save multiple birth charts
- Track personal predictions
- Store preferences

---

**This demo shows the complete flow of the AstrologyApp!** 🚀
