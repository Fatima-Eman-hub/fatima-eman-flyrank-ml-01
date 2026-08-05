# Study Coach — a source-grounded AI study agent

## What it does, and for whom

Study Coach turns instructor lecture slides into exam-ready study notes,
and then quizzes you on them — grounded strictly in your own source
material via a live Google Drive connection, not general knowledge. Built
for students who want active-recall practice without manually retyping
notes into a study app.

## Setup (a stranger could follow this)

1. Create a free Claude.ai account at claude.ai.
2. Go to **Settings → Connectors → Add → Google Drive**, and authorize it.
3. Go to **Projects → Create project**. Name it "Study Coach."
4. Paste this into the Project's custom instructions:

   > You are my study coach. When I name a topic or slide, first locate
   > the source file via Google Drive search. Read it, then produce study
   > notes in this format: Definition, Why It Works (analogy), Key Facts,
   > Exam Trap — one card per distinct concept. Before returning the
   > result, count how many distinct concepts the source actually
   > contains and compare that to how many cards you produced. If they
   > don't match, say so explicitly and re-generate the missing card(s)
   > rather than silently returning an incomplete set. If a source file
   > is a scan with no extractable text, switch to reading it visually
   > rather than returning a failed extraction as if it were content. If
   > any fact is unclear or illegible, flag it as uncertain rather than
   > guessing. When I ask to be quizzed on a topic, only generate
   > questions from notes and source content already produced in this
   > conversation — never invent unrelated content.

5. Upload your lecture slides to Google Drive (any folder).
6. Start a new chat inside the Project.

## Usage examples

- `Give me study notes on Decision Trees from my slides in Google Drive.`
- `Quiz me on Decision Trees.`

## Architecture