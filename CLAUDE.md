# CLAUDE.md

## What this project is

We are building "the Hebrew Diary of a CEO", a Hebrew video podcast of about an hour per episode that interviews Israeli cybersecurity CEOs and founders. It is recorded at the RHEL Guts Innovation Hub. We want the views and viral short clips that The Diary of a CEO (Steven Bartlett) and the Jack Neel Podcast get.

This repo holds the research, the principles and the per-guest prep that the production team and the host use before each recording. There is no code here.

## Language

All deliverable files are in Hebrew, because the podcast is in Hebrew. CLAUDE.md and the README are in English. Research can be done in either language. Company names, podcast names and clip titles keep their original spelling (Armis, The Diary of a CEO).

## Files

- `01-principles-viral-clips.md`: interview principles only. Each interviewer (Bartlett, Neel, Stebbings, the Acquired hosts, Rhysider) gets a numbered list of specific principles with no links. Then comes a second numbered list in which item N shows principle N with a real YouTube Short, quoting what is said in it. The two lists have no sub-titles. Short sections on preparation and studio rules close the file.
- `02-podcasts-to-study.md`: who each interviewer is, what he does and why he matters to us. No links.
- `03-<guest>-guest-data.md`: static facts about the guest. Bio, timeline, numbers, past quotes to confront him with, comparisons with other CEOs, previous interviews, sources. Current file: `03-nadir-izrael-guest-data.md`.
- `04-<guest>-questions.md`: bullet points of questions only, grouped by act, with follow-ups nested under them. After the questions comes the pre-show checklist for that guest. Current file: `04-nadir-izrael-questions.md`.
- `05-editing-principles.md`: editing principles in the same two-list format as 01. Covers short clips, titles, the full episode and trailer, thumbnails and distribution.

## Evidence and links

Every principle in 01 and 05 needs a demonstration. Use a real YouTube Short (never TikTok) from one of the five model podcasts, and say exactly what happens in it, preferably quoting the host's question or the clip's first line. When no Short can show the principle (silence, research habits, thumbnail tests), cite the article it comes from instead. Use verified URLs only.

Real Shorts with view counts come from a channel's YouTube RSS feed. Popular Shorts: `https://www.youtube.com/feeds/videos.xml?playlist_id=UUPS<channel id without "UC">`. Latest uploads: `?channel_id=<id>`. Channel IDs:

- DOAC `UCGq-a57w-aPwyi3pW7XLiHw`
- DOAC Clips `UCnjgxChqYYnyoqO4k_Q1d6Q`
- Jack Neel `UCFRCiFkWWJN2rO6dsKU9-1A`
- 20VC `UCf0PBRjhf0rF8fWBIxTuoWA`
- Acquired `UCyFqFYfTW2VoIQKylJ04Rtw`
- Darknet Diaries Clips `UCXnxYgJ52Jwx9LAa-ARWjEg`

Transcripts can be pulled with the `youtube-transcript-api` Python package. YouTube blocks the IP (`IpBlocked`) if you fetch fast, so leave several seconds between requests.

List sources at the end of each file. Mark secondhand figures as such, and write "(לאמת)" next to any guest fact that still needs checking.

## Length and tone

Write short. A principle is a general rule that says what to do and when. It contains no example: no sample question, quote or wording. Examples belong only in the demonstration list that follows, and each demonstration is a real clip or source. Leave out explanations of why something works and any intro about what the document is. The questions file can be long because it has to fill an hour plus backups.

## Writing that does not read as AI-generated

These are the 20 most common tells of AI-written text, compiled from Wikipedia's "Signs of AI writing" guide and Pangram's frequency data. None of them should appear in any file in this repo, Hebrew or English.

1. Stock AI vocabulary. English: delve, crucial, pivotal, tapestry, testament, showcase, landscape, robust, seamless, leverage, navigate. Hebrew: "חשוב לציין", "בעולם של היום", "מסע", "מרתק", "פורץ דרך", "מגוון רחב", "שלל", "מהווה".
2. Inflated significance: calling things a "turning point", "a testament to" something, or saying they "set the stage" or "leave a legacy".
3. Promotional tone: "vibrant", "rich", "boasts", "nestled", "world-class", "unique", and their Hebrew equivalents.
4. Tacked-on analysis clauses: "..., highlighting X", "..., reflecting Y", or in Hebrew "..., מה שמדגיש/ממחיש".
5. Negative parallelism: "not X but Y", "it's not just X, it's Y", "X rather than Y". In Hebrew, "לא X אלא Y". State the positive claim directly.
6. Triads: packing items, adjectives or examples into threes by habit. Use the number of items the content actually has.
7. Em dashes, or spaced en dashes used the same way. Use a comma, a colon, parentheses or a new sentence.
8. Avoiding plain "is": "serves as", "functions as", "stands as". In Hebrew, "מהווה". Write "is", or "הוא/היא".
9. Vague attribution: "experts say", "studies show", "many believe". Name the source or drop the claim.
10. Stacked hedges and disclaimers: "it's worth noting", "generally speaking", "while details are limited".
11. Formulaic wrap-ups: "In conclusion", "Overall", "Bottom line", or a closing summary that repeats the content.
12. Chatbot phrasing: "Certainly!", "Great question", "I hope this helps", "Let me know if...".
13. Too much bold. Bold almost nothing.
14. Inline-header lists, where every bullet starts with a bold label and a colon. Write the sentence instead.
15. Emoji used as formatting (✅ 🚀 🔥 ▶️ 📄 ⚠️ 🟢 and so on).
16. Unusual Unicode: arrows (→ ← ↳), ≈, ⚠, box-drawing characters, decorative bullets such as "·".
17. Lists and tables where prose works better, such as a table for two or three facts or bullets that should be one sentence.
18. Meta structure: intros like "This document explains...", a heading over every few lines, Title Case headings.
19. Uniform rhythm and synonym cycling: every sentence the same length, or a new synonym each time for the same thing. Vary sentence length and reuse the same word.
20. Unverifiable content: invented or broken links, placeholders (XX, "INSERT"), or claims that can't be traced to a source.

## Question-writing rules (04)

- One question per line. Never ask a double question ("שאלה כפולה"), meaning two questions in one sentence, such as "What did you learn at Google, and how did it shape Armis?". The guest answers one half and the answer can't be clipped. Ask the main question, then each follow-up separately. Whenever a file mentions a double question, explain what it is.
- Ask for stories over opinions. Keep questions to about 12 words. Ask for numbers, places, names and feelings.
- The order follows the DOAC arc: an opening hook, childhood, the road, the peak and what it cost, cyber and AI, Israel, a speed round, and the closing ritual (the guest answers a question left by the previous guest and writes one for the next).
- The file holds questions only. Stage directions go in parentheses, such as "(שתיקה)" or "(מקרינים קטע)". The facts behind the questions live in the guest-data file.
- Use the techniques from 01: an opener with a number; warm questions before hard ones; "take me to that moment" (Rhysider); a best-ever question followed by "how much?" (Stebbings); yes/no and agree/disagree questions (Neel); asking "can I push back?" and then "help me understand" with a past quote (Stebbings, Bartlett); comparing him with another CEO (Stebbings); a prediction with a year (Bartlett); "explain it to my mom"; "say that in one sentence"; a game (Neel); a legacy question.
- Before writing, listen to and read the guest's previous interviews in Hebrew and English. Skip questions he has already answered and go further than those interviews did.

## Pre-show checklist (end of 04)

Agree on these with every guest before recording:

1. The format: the opening, five acts, a speed round with one-word to one-sentence answers, and the closing ritual. Ask him to prepare a question for the next guest.
2. How we want him to answer. He leads with the bottom line and repeats the subject of the question, so each answer works as a clip without the question. He tells specific stories with numbers, explains any jargon on the spot, says it in Hebrew rather than English tech slang, and never says "as I said earlier". He may restart an answer or refuse one. He looks at the host, not the camera.
3. Sensitive topics, each marked allowed, allowed with conditions, or off limits: family; partner and children; health; personal money; religion; military service (military censorship applies); customers under NDA; specific attacks and state actors; the acquirer, a public company, so no inside information; deal details; board and investors; layoffs; competitors; the co-founder; politics and the war; living abroad; satire about him, including the rights to any clip we show; how much he paid personally; angel investments. Off-limits topics are not asked and are cut if they come up.
4. Legal and PR. He signs a release form. He does not approve clips in advance, but he has 48 hours to flag factual, security or legal errors. Agree on who from PR attends, any embargo dates, and a censorship check if military details came up.
5. Fact-check every item marked "(לאמת)", plus his on-screen name, title and pronunciation.
6. Props he brings, such as a childhood photo or a photo from the company's first days.
7. The day itself: arrive 30 minutes early, plain-coloured clothes, phone off, and 10 minutes of off-camera talk that stays away from the questions.
8. Distribution: his and the company's handles, a promise to share within the first hour after release, and a thank-you email the same evening.

## Current guest

Nadir Izrael (נדיר יזרעאל), co-founder and CTO of Armis. ServiceNow bought Armis for $7.75B; the deal was signed in December 2025 and closed in April 2026. He grew up in Kiryat Ata. His mother was disabled in a car accident before he was born. He went to a yeshiva high school, served in Unit 8200, studied at the Technion and worked at Google. The Eretz Nehederet character "Nadir Ackerman" is named after him. See `03-nadir-izrael-guest-data.md` and `04-nadir-izrael-questions.md`.
