# 🎮 League of Legends Game Analytics Web App

This is a PHP & MySQL-based web application designed to provide interactive analytics for League of Legends players.  
The platform enables users to explore player statistics, match data, achievements, and session trends through a user-friendly interface.

---

## 📂 Project Structure

```plaintext
lol-analytics/
├── index.php                   # Landing home page
├── create_tables.sql           # SQL schema (DDL)
├── insert_data.sql             # Sample data population (DML)
├── config/
│   └── db.php                  # Database connection configuration
├── pages/
│   ├── leaderboard.php         # Top players by gold earned
│   ├── player_achievements.php # Player achievements (JOIN query)
│   ├── analytics.php           # Aggregated stats (AVG, COUNT)
│   ├── update_profile.php      # Player profile update
│   ├── delete_player.php       # Player deletion with cascading
│   ├── dashboard.php           # Chart.js visualizations
│   ├── trend_data.php          # AJAX endpoint for trend data
│   └── navbar.php              # Shared navigation bar
├── styles/                     # CSS styles for individual pages
    ├── index.css
    ├── leaderboard.css
    ├── player_achievements.css
    ├── update_profile.css
    ├── delete_player.css
    ├── dashboard.css
    ├── analytics.css
    └── navbar.css

```

---

## 🚀 How to Run the Application

### 📦 Prerequisites

- A local web server environment (e.g., XAMPP, MAMP, or WAMP)
- PHP 7.x or higher
- MySQL or MariaDB
- A modern web browser

### 🛠 Setup Instructions

1. **Start Apache and MySQL** using your local server control panel.
2. **Set up the database:**
   - Open `phpMyAdmin` or your preferred MySQL client.
   - Create a database named `lol_analytics_cs5200`.
   - Import the schema from `create_tables.sql`.
   - Populate the database with sample data using `insert_data.sql`.
3. **Configure the project:**
   - Place the `lol-analytics/` folder in your web server's root directory (e.g., `htdocs/` for XAMPP).
   - Update the database credentials in `config/db.php` to match your local setup.
4. **Run the application:**
   - Open your browser and navigate to `http://localhost/lol_analytics/index.php`.

---

## 🖥️ Application Features

| Feature                    | Description                                                                 |
| -------------------------- | --------------------------------------------------------------------------- |
| 🏆 **Leaderboard**         | Displays the top 5 players by total gold earned.                            |
| 🎯 **Player Achievements** | Lists player achievements with detailed descriptions.                       |
| 📊 **Analytics Dashboard** | Provides aggregated statistics such as average playtime and total matches.  |
| 🛠 **Update Profile**       | Allows users to update player profiles, including rank and region.          |
| 🗑 **Delete Player**        | Enables deletion of player accounts with cascading removal of related data. |
| 📈 **Visual Dashboard**    | Interactive charts (bar, pie, and line) powered by Chart.js.                |
| 🧭 **Navigation Bar**      | A shared navigation menu for seamless access to all features.               |

---

## 📈 Key Analytical Queries

The application leverages SQL queries to provide insights into player performance and match trends. Examples include:

- **Join Queries:** Displaying player achievements with detailed descriptions.
- **Aggregations:** Calculating average playtime and total matches per player.
- **Nested Aggregations:** Summarizing total playtime per player per week.
- **Filtered Queries:** Identifying top players by specific metrics (e.g., gold earned).

---

## 🛠️ Technologies Used

- **Backend:** PHP (PDO for database interaction)
- **Database:** MySQL
- **Frontend:** HTML, CSS, JavaScript (Chart.js for visualizations)
- **AJAX:** Dynamic data loading for trend analysis
