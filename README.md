# Streamverse - Ultimate Video Streaming (Intelligent Edition v2.1)

Streamverse is a feature-rich, single-page video streaming application built entirely with front-end technologies (React, JavaScript, HTML, CSS) and utilizing SQLite.js for in-browser data persistence. It simulates an intelligent streaming platform with features like user authentication, multiple profiles, personalized recommendations, watch history, favorites, comments, subscription tiers, and dynamic theming.

**Live Demo Note:** This application is designed to run directly in a modern web browser. Open the `app.html` file.
![app](https://github.com/user-attachments/assets/8779d99f-65cd-4348-87d4-7f278598febf)


## Features


### Core User Experience
*   **User Authentication:** Secure (simulated) sign-up and login functionality.
*   **Profile Management:**
    *   Support for up to 5 user profiles per account.
    *   Create, edit, and delete profiles.
    *   Customizable profile name and avatar.
    *   Child profile option with associated parental controls.
*   **Video Playback:**
    *   Embedded video player with standard controls.
    *   Tracks and resumes playback progress.
    *   Poster images for videos.
*   **Content Discovery:**
    *   Dynamic Hero section showcasing featured content.
    *   "Continue Watching" row for quick access to in-progress videos.
    *   "Recommended For You" row (simulated AI-driven based on viewing habits).
    *   Browse content by genre.
    *   Dedicated pages for "TV Shows," "Movies," and simulated "Live" content.
*   **Search Functionality:** Search videos by title, description, genre, or tags.

### Engagement & Personalization
*   **Video Details Page:**
    *   Comprehensive information: title, description, year, duration, genre, rating, views, content rating.
    *   Like/Dislike reactions with counts.
    *   Add to/Remove from Favorites.
*   **Comments Section:** Users can post and view comments on videos (profile-specific).
*   **Favorites List:** Each profile can maintain its own list of favorite videos.
*   **Parental Controls:**
    *   Content filtering based on profile's selected content rating (G, PG, PG-13, R, NC-17).
    *   Child profiles have restricted content rating options.
*   **Dynamic Theming:**
    *   Switch between Light and Dark themes.
    *   Theme preference is saved per profile and globally.
*   **In-App Notification System:**
    *   Displays non-intrusive notifications for recommendations, new episodes (simulated), and system messages.
    *   Notifications are styled by type (info, success, warning, error).

### Subscription & Settings
*   **Subscription Tiers:**
    *   Simulated Basic, Premium, and Professional subscription plans.
    *   Feature differences clearly outlined.
    *   Simulated payment process for upgrading tiers.
*   **Comprehensive Settings Page:**
    *   View user account details (username, email, join date, current subscription).
    *   Manage all user profiles.
    *   Configure profile-specific preferences:
        *   Parental control level.
        *   Autoplay next episode.
        *   Default video quality.
        *   Preferred audio language.
        *   Notification preferences (new episodes, recommendations, live events, notification email).
    *   Global theme toggle.

### "Intelligent" Simulated Features
*   **Dynamic Hero AI:** Highlights relevant or high-rated content.
*   **Personalization AI:** Tailors experience based on profile data and preferences.
*   **Intelligent Curation Engine (ICE):** Simulates AI considering viewing patterns, ratings, etc., for recommendations.
*   **Advanced Social Features (AI-Powered Comments - placeholder):** Hints at future sentiment analysis, topic clustering.
*   **Intelligent Playback (Adaptive Bitrate - simulated):** Placeholder for future adaptive streaming.
*   **AI-Powered Semantic Search (placeholder):** Future capability for more natural language search.
*   **Content Ingestion & AI Tagging (placeholder):** Simulates backend processes for new content.
*   **AI-Enhanced Live Events (placeholder):** Ideas for interactive live experiences.
*   **AI-Driven Subscription Offers (placeholder):** Concept for personalized plan recommendations.

## Technologies Used

*   **HTML5:** Structure of the application.
*   **CSS3:** Styling, responsiveness, and theming (using CSS Variables).
*   **JavaScript (ES6+):** Core application logic.
*   **React (v18):**
    *   UI library for building components.
    *   Utilizes Hooks extensively: `useState`, `useEffect`, `useContext`, `useRef`, `useCallback`.
    *   Context API for global state management.
*   **Babel (Standalone):** For in-browser JSX and modern JavaScript transpilation.
*   **SQLite.js (sql.js v1.10.3):**
    *   SQL database engine compiled to WebAssembly.
    *   Allows running SQLite queries directly in the browser.
    *   Database is persisted in `localStorage`.
*   **Font Awesome (v6.5.1):** For icons.
*   **Google Fonts:** For typography (`Open Sans`, `Roboto`).

## Setup and Usage

1.  **Download:** Get the `app.html` file.
2.  **Internet Connection:** Required for loading CDN resources (React, Babel, Font Awesome, SQL.js WASM).
3.  **Open in Browser:** Open the `index.html` file in a modern web browser (e.g., Chrome, Firefox, Edge, Safari).

### How to Navigate the App:

1.  **Initial Load:** The app will initialize the database (may take a moment on first load or if `localStorage` is cleared).
2.  **Sign Up/Login:**
    *   Click the user icon in the navbar.
    *   Choose to "Sign Up" for a new account or "Login" with existing (simulated) credentials.
3.  **Profile Selection:**
    *   After login, you'll be prompted to "Choose Who's Watching" or create a new profile if none exist.
4.  **Explore:**
    *   The **Home** page displays a hero video and rows of content categorized by genre, recommendations, and continue watching.
    *   Use the navbar links for **TV Shows**, **Movies**, and **Live** (simulated) sections.
5.  **Search:** Type in the search bar (visible after selecting a profile) and press Enter.
6.  **Watch Videos:** Click on any video card to navigate to the player page.
7.  **Interact:**
    *   On the player page, you can like/dislike, add to favorites, and post comments.
    *   Video progress is automatically saved.
8.  **Manage Settings:**
    *   Click your profile name/avatar in the navbar or navigate to `#/settings`.
    *   Manage account details, profiles, parental controls, playback preferences, notification settings, and the global theme.
9.  **Subscription:**
    *   Navigate to `#/subscription` (or via Settings) to view available plans and simulate an upgrade.

## Key Concepts & Design

*   **Single-File Application:** All HTML, CSS, and JavaScript (transpiled by Babel) are contained within a single `index.html` file for ease of deployment and demonstration.
*   **Client-Side Rendering & Logic:** The entire application runs in the user's browser. React handles UI rendering, and all data operations (including database interactions) are client-side.
*   **In-Browser Database (SQLite.js):**
    *   A full-fledged SQL database is implemented using SQL.js, with the database file exported and stored in the browser's `localStorage`.
    *   This allows for complex data relationships and querying without a backend, with data persisting across sessions for that specific browser.
*   **Component-Based Architecture:** The UI is built using reusable React components.
*   **Global State Management (Context API):** React's Context API is used to manage global state such as the current user, active profile, theme, modal visibility, and notifications.
*   **Simulated Backend Operations:** Features that would typically require a backend (e.g., payment processing, real-time AI, user data storage beyond `localStorage`) are simulated to demonstrate a complete application flow.
*   **Parental Controls:** A practical implementation of content filtering based on user-defined profile settings and video metadata.
*   **Responsive Design:** The UI adapts to different screen sizes, from mobile to desktop.

## Notes & Limitations

*   **No Backend Server:** This is a front-end-only application. All data, including user accounts and watch history, is stored in the browser's `localStorage`. Data is not shared across devices or browsers.
*   **Simulated Features:** Critical features like payment processing, live streaming, and advanced AI-driven recommendations are simulated for demonstration.
*   **Security:**
    *   Password "hashing" is trivial (`hashed_password`) and **NOT SECURE** for any real-world application. Production systems require strong, salted, server-side hashing.
    *   No real user data is transmitted over a network.
*   **Performance & Scalability:**
    *   `localStorage` has size limitations (typically 5-10MB). Very large amounts of video metadata or user data could exceed this.
    *   Complex SQL.js queries on large datasets might affect browser performance.
    *   Not designed for large-scale, multi-user production deployment without a proper backend infrastructure.
*   **CDN Dependencies:** The application relies on Content Delivery Networks for React, Babel, Font Awesome, and the SQL.js WASM file. An internet connection is required for these to load.

## Potential Future Enhancements

*   Integration with a real backend (e.g., Node.js/Express, Python/Django/Flask, Firebase) for:
    *   Persistent user data across devices.
    *   Secure authentication.
    *   Actual video hosting and streaming.
    *   Real payment gateway integration.
*   Development of genuine AI/ML models for recommendations, semantic search, and content analysis.
*   Implementation of real-time features like live chat during streams.
*   More robust error handling and user feedback mechanisms.
*   An administration panel for content management.

## Credits

Developed by [Slogan Technologies](https://bit.ly/slogantechnologies) (as simulated in the application footer).
Video content samples are from open sources like Blender Foundation and Google.
Placeholder images from Picsum Photos.
