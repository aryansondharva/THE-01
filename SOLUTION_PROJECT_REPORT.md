# Aura - Project Report

## The Problem

We noticed a simple problem among our friends - **they study hard but forget fast**.

We talked to 10 students from our college. Most of them said:
- "I read the same thing again and again before exams"
- "I don't know which topics I'm weak in"
- "Making flashcards takes too much time"

One friend told us he reads his notes 4 times before every exam because he keeps forgetting. Another friend spent 3 hours just making flashcards for one chapter.

**The main issue:** Students don't have a simple way to know what to revise and when to revise it.

---

## What We Learned

We first thought students just need more quiz questions. But when we showed our early app to our friends, they told us:

- "Don't make me organize topics - do it automatically"
- "Show me what I'm bad at"
- "Tell me when I should revise"

So we changed our app based on their feedback.

---

## Our Solution

**Aura is simple:** Upload your PDF → Get quizzes → See your weak topics → Know when to revise.

### How it works:

1. **Upload PDF** - Upload any study notes or textbook chapter
2. **Auto Topics** - App breaks it into small topics automatically
3. **Take Quiz** - 10 questions, 10 minutes timer
4. **See Results** - Score + which topics are weak
5. **Get Reminder** - App tells you when to revise (based on your score)
6. **Flashcards** - Quick revision cards made from your wrong answers

---

## Testing Results

We tested with 10 students for 2 weeks:

| What happened | Numbers |
|---------------|---------|
| Students who used it regularly | 4 out of 10 |
| Average score improvement | +2 points |
| Students who want to keep using it | 4 out of 10 |

**What students liked:**
- Auto topic creation (saves time)
- Seeing weak topics highlighted
- Flashcards from wrong answers

**What needs fixing:**
- Big PDFs are slow
- Mobile view not good
- Needs internet to work

---

## What's Next

If we continue:
- Make a mobile app
- Add revision reminders
- Let friends study together
- Support Hindi language

---

## Tech Used

- Frontend: React
- Backend: Node.js
- Database: Supabase
- AI: Groq, Gemini

---

## How We Built It (AI Tools & Our Process)

We used Kiro IDE throughout for coding assistance and autocomplete. ChatGPT helped us figure out the PDF text extraction - took us 4-5 tries before we got the chunking right for topic generation.

The quiz generation prompt was tricky. We started with a basic prompt from Claude but the questions were too generic. We rewrote it 3 times until the MCQs actually made sense with proper options.

Database schema started as a Gemini suggestion but we changed it completely after realizing we needed separate tables for quiz attempts and answers. Learned that the hard way when our progress tracking broke.

The spaced repetition logic was mostly us - lots of reading about Ebbinghaus forgetting curve and trial and error with the review date calculation. We tried using a fixed formula first, then switched to a simple ML approach after testing showed fixed intervals don't work for everyone.

LangChain integration was painful. Docs were confusing, spent 2 days just getting Groq and Gemini to work together with fallback. Stack Overflow and GitHub issues saved us there.

The flashcard generation feature came from a friend's suggestion during testing. We built it in one night using the same LLM setup we already had.

Frontend animations and 3D visual? YouTube tutorials + Framer Motion docs + lots of copy-paste-modify until it looked decent.

---

*Based on feedback from 10 students we talked to personally.*
