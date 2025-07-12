# 🎬 Movie Discovery App

A sleek, modern React-based movie discovery application that allows users to search for thousands of movies, explore trending titles, and track search trends using Appwrite's backend services.

---

## 🔥 Features

- 🔍 **Live Search** for movies using TMDB API  
- 📈 **Trending Movies** based on most searched terms (powered by Appwrite database)  
- 🎨 Beautiful **Tailwind CSS**-based UI with responsive design  
- ⏳ Debounced API requests for optimized performance  
- 🧠 Simple usage analytics with Appwrite (track top searches)  
- 🌐 External API: The Movie Database (TMDB)

---

## 🛠 Tech Stack

| Frontend    | Backend        | Styling     | Deployment               |
|-------------|----------------|-------------|---------------------------|
| React.js    | Appwrite (DB)  | Tailwind CSS | Vite                      |
| JavaScript  | Appwrite SDK   | Custom CSS  | Optional: Netlify/Vercel |

---

## 🧑‍💻 Local Setup

### 1. Clone the Repo

```bash
git clone https://github.com/your-username/movie-discovery-app.git
cd movie-discovery-app
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Set Up `.env.local`

Create a `.env.local` file in the root directory:

```env
VITE_TMDB_API_KEY=your_tmdb_api_key
VITE_APPWRITE_PROJECT_ID=your_appwrite_project_id
VITE_APPWRITE_DATABASE_ID=your_appwrite_database_id
VITE_APPWRITE_COLLECTION_ID=your_appwrite_collection_id
```

### 4. Start the Dev Server

```bash
npm run dev
```

Visit `http://localhost:5173` to view the app.

---

## 🗃 Appwrite Configuration

This project uses Appwrite's **Database API** to:

- Store and update search terms
- Track the `count` of searches per term
- Retrieve top 5 trending movies based on search frequency

### Expected Collection Schema

| Field         | Type     | Required |
|---------------|----------|----------|
| `searchTerm`  | String   | ✅        |
| `count`       | Integer  | ✅        |
| `movie_id`    | String   | ✅        |
| `poster_url`  | String   | ✅        |

---

## 📁 Project Structure

```bash
├── public/
│   └── assets (icons/images like search.svg, No-Poster.png)
├── src/
│   ├── components/
│   │   ├── MovieCard.jsx
│   │   ├── Search.jsx
│   │   └── Spinner.jsx
│   ├── appwrite.js        # Appwrite integration logic
│   ├── App.jsx            # Main component
│   └── index.css          # Tailwind and global styling
└── .env.local             # Environment variables
```

---

## 🧠 Future Improvements

- User authentication with Appwrite  
- Save favorite movies per user  
- Infinite scroll / pagination for search results  
- Filter by genre, language, year, etc.  
- Dark/light theme toggle  

---

## 📸 Screenshots

<img width="2990" height="1484" alt="image" src="https://github.com/user-attachments/assets/076c99c2-dfbb-4f51-9d43-a844099d594c" />
<img width="2988" height="1492" alt="image" src="https://github.com/user-attachments/assets/1d52cae3-67e4-434b-adc2-d79c9bce14ce" />

---

## 📝 License

MIT License. Feel free to fork and modify.
