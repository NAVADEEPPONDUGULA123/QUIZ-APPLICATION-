# Quizly — Quiz Application

A responsive student-level Quiz Application built with **React and Vite**. It lets users choose quiz categories, answer multiple-choice questions, view results, add their own questions, and keep their best scores between visits.

## Features

- **Quiz categories:** General Knowledge, Science, Technology, Mathematics, Sports, and History.
- **Question screen:** Four answer options, question progress, answer selection, and score tracking.
- **Results screen:** Final score, percentage, correct/incorrect count, and a play-again action.
- **Custom question form:** Add a question, four options, choose the correct option, and select a category.
- **Public quiz API:** Fetches questions from the [Open Trivia Database](https://opentdb.com/).
- **Offline fallback:** If the API is unavailable or has no suitable questions, the app uses built-in sample questions and saved custom questions.
- **Persistent data:** Custom questions and best scores are stored in browser `localStorage` and remain after restarting the app.
- **Responsive interface:** Works on desktop, tablet, and mobile screens.

## Technology

- React 18
- Vite
- JavaScript (ES modules)
- CSS
- Open Trivia Database API
- Browser `localStorage`

## Project structure

```text
quiz-application/
├── public/
│   └── favicon.svg
├── src/
│   ├── components/
│   │   ├── AddQuestion.jsx
│   │   ├── Header.jsx
│   │   ├── QuestionCard.jsx
│   │   ├── Results.jsx
│   │   └── StatCard.jsx
│   ├── data/
│   │   ├── categories.js
│   │   └── sampleQuestions.js
│   ├── utils/
│   │   ├── api.js
│   │   └── storage.js
│   ├── App.jsx
│   ├── main.jsx
│   └── styles.css
├── .gitignore
├── index.html
├── package.json
├── vercel.json
├── vite.config.js
└── README.md
```

## Run locally

1. Install **Node.js LTS**.
2. Download or clone this repository.
3. Open a terminal in the project folder.
4. Install dependencies:

   ```bash
   npm install
   ```

5. Start the development server:

   ```bash
   npm run dev
   ```

6. Open the local URL shown in the terminal (usually `http://localhost:5173`).

## Build for production

```bash
npm run build
npm run preview
```

Vite creates the production website in the `dist` folder.

## GitHub upload

Create a new repository on GitHub, then run these commands from the project folder:

```bash
git init
git add .
git commit -m "Add Quizly quiz application"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
git push -u origin main
```

Replace the remote URL with your own GitHub repository URL.

## Deploy on Vercel

1. Push the project to GitHub.
2. Sign in to [Vercel](https://vercel.com/) using GitHub.
3. Select **Add New → Project**.
4. Import your Quizly GitHub repository.
5. Vercel detects Vite automatically. Confirm these settings:

   | Setting | Value |
   |---|---|
   | Framework Preset | Vite |
   | Build Command | `npm run build` |
   | Output Directory | `dist` |
   | Install Command | `npm install` |

6. Select **Deploy**. Vercel will provide your live website URL.
7. Future pushes to the connected GitHub branch trigger new deployments.

## API details

The app requests multiple-choice questions from:

`https://opentdb.com/api.php?amount=10&category={categoryId}&type=multiple`

Open Trivia Database is a public service. The app handles loading errors and falls back to local questions when the API cannot provide questions. No API key is required.

## Data storage

The app uses these browser storage keys:

- `quizly_custom_questions` — questions created by the user.
- `quizly_best_scores` — best score for each category.

Data is stored in the current browser on the current device. Clearing browser site data or using another browser/device will not carry these records over.

## Assignment requirement checklist

- [x] List of quiz categories
- [x] Question screen with multiple-choice options
- [x] Score tracking
- [x] Results screen
- [x] Form to add custom questions
- [x] Questions from a public quiz API
- [x] Questions saved on the device
- [x] Best scores persist after app restarts
- [x] GitHub-ready source code
- [x] Vercel deployment configuration

## License

This project is provided for educational and student project use.
