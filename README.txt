WHAT'S NEW (latest)
  - Lesson search in MCQ AI: "lesson <name>" lists that lesson's questions (practice / slideshow / "Ask me one by one"),
    "ask lesson <name>" asks them one at a time. Works in Bangla too (পাঠ / অধ্যায়). Lesson names come from q-manifest.js.
  - "same" (also "same one", "same type", "একই") shows another question related to the current / last one.
  - MCQ AI topics are now read from q-manifest.js every time (sub-category names, lesson names, bilingual names such as
    "জরিপ (Surveying)", plus small typos like "surveing"). A sub-category you add later works with no code change.
  - "Ask about <word>" works even when the word is not a sub-category: it asks questions that mention that word.
  - When AI cannot find something it shows tappable "Subjects in your bank" buttons instead of a dead end.
  - New prompts: revise, new subjects, find <word> / where is <word>.
  - Daily: after Next the new question is scrolled to the top (works in any scroll container, no keyboard jump).

MCQ Master - mobile web app (PWA)

FILES
  index.html, script.js, style.css     the app
  sw.js, manifest.webmanifest,   make it installable + offline
  q-manifest.js, q-*.js                your questions
  check.html                           data checker (open it to validate the q-*.js files)

HOW TO USE
  1. Upload the whole folder to any HTTPS host (GitHub Pages, Netlify, Cloudflare Pages, Vercel).
     Installing and offline mode do not work from file://. For a local test run:
        python3 -m http.server 8000      then open http://localhost:8000
  2. Open the site on your phone:
        Android/Chrome: tap the "Install" card (or browser menu > Install app)
        iPhone/Safari : Share > Add to Home Screen

UPDATING QUESTIONS
  Edit/add q-*.js, update q-manifest.js, and change the "v" number in q-manifest.js.
  Phones then download the new data automatically and show a "new version" bar.

WHAT'S NEW
  - MCQ AI is now dynamic: every sub-category in q-manifest.js works automatically (for example "Ask about surveying", "জরিপ").
    The category/sub-category of each question comes from q-manifest.js, not from the header inside q-*.js.
  - Ask mode: "Ask question" / "Ask about <topic>" shows a question. Type A/B/C/D or the answer itself,
    "explain" shows answer + explanation, "next" shows a related question.
  - New prompts: related, I don't know, current question, question 3, how many correct, lessons of <topic>,
    random question, unseen questions, study plan, subject stats, explain all, how does ask work.
  - Daily: after Next, the new question scrolls to the top of the screen.
  - Search bar: focus glow, sweeping light line, pulsing icon while searching, typing placeholder, result cards slide in.
  - MCQ AI: 50 new prompts (say "commands" in the chat to see and tap them all):
      Quiz: repeat, 50 50, show answer, previous, restart, how many left, accuracy, streak, quiz mistakes,
            quiz skipped, slide these, practice these, harder, easier, swap question, time taken, reset score
      Sets: answers, answer 3, explain 3, set again, Next 10 without answers, then "1-B 2-A 3-C" to get marked
      Stats: my progress, best score, average score, last exam, how many wrong, weakest subject,
             strongest subject, list subjects, topics of math, daily status
      Pages: open search / history / bank / practice / daily / slider / read / add question / go home
      Extras: motivate me, study tip, what is the date, clear chat, surprise me, thanks, bye
      Most also work in Bangla, for example: আগের প্রশ্ন, আমার অগ্রগতি, সার্চ খোলো, শেষ পরীক্ষা, দুর্বল বিষয়.
  - MCQ AI chat: Ask question, Ask about math, Next 10, Random 10, Mix 10 (numbered MCQs + answer key), typing animation.
  - Question Slider: 15 s option added; phone Back now closes the More menu first.
  - Exam setup page redesigned (summary tiles, steppers, cut-mark selector).
  - More > MCQ AI: chat that reads the whole question bank (works offline).
    Optional: tap the gear and add a Google Gemini API key (free at aistudio.google.com/apikey) to answer anything.
  - More > Question Slider: timed slideshow (30/60/90/120 s), answer + explanation, swipe or arrow keys.
  - General Knowledge (English) category removed; Math added (Arithmetic, Algebra, Geometry, Mensuration).

NOTE
  All files listed in q-manifest.js are present (24 files, 2,525 questions). Open check.html after any change to validate them.
