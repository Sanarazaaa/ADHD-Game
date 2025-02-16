# 🎮 ADHD Game

A fun and interactive bubble-popping game built using **HTML**, **CSS**, **JavaScript**, and **D3.js**, with automatic score tracking and data logging to **Google Sheets**.

## 📝 Description

In this game, players pop bubbles to earn points. Larger circles award **+5 points**, while smaller circles are worth **+20 points**. The game ends if a player fails to pop any small circle for **2 consecutive minutes**.

## 📊 Features

- **Dynamic Circle Generation:** Randomized circle sizes and positions with interactive popping.
- **Scoring System:** Big Circle = +5 points, Small Circle = +20 points.
- **Difficulty Scaling:** Circles fade faster as the score increases.
- **Game Over Condition:** The game ends if a small circle is not popped for 2 minutes.
- **Audio Feedback:** Pop sound plays when a circle is clicked.
- **Google Sheets Integration:** Automatically logs scores in Google Sheets.

## 🛠️ Technologies Used

- **HTML5** – Structuring the game interface.
- **CSS3** – Styling and background gradients.
- **JavaScript (ES6)** – Game logic and real-time user interactions.
- **D3.js** – SVG circle creation and animations.
- **Google Colab** – Hosting and executing the game.
- **Google Sheets API** – Automating score logging.
- **Event Handling** – Tracking user clicks and circle removal.
- **Animation** – Implementing smooth transitions and fade-outs.

## 🚀 How to Run the Game

1. Open **Google Colab** and create a new notebook.
2. Add an HTML cell and paste the game code.
3. Set up Google Sheets integration with the following Python code:

    ```python
    from google.colab import auth
    import gspread
    from oauth2client.client import GoogleCredentials

    auth.authenticate_user()
    gc = gspread.authorize(GoogleCredentials.get_application_default())

    worksheet = gc.create('Circle Pop Scores').sheet1
    worksheet.append_row(['Score'])

    def save_score_to_sheet(score):
        worksheet.append_row([score])
    ```
4. Click **Run** to start the game.

https://github.com/user-attachments/assets/d6b37808-c466-45ac-ba6d-c1c89417e4fc

9de82c-c8bc-4b60-8322-9cc2b4d69448)


## 📌 Future Enhancements

- Leaderboard for high scores.
- Customizable difficulty levels.
- Multiplayer mode.

## 📄 License

This project is licensed under the **MIT License**.
