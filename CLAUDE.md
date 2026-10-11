# CLAUDE.md

## What this project is

We are building "the Hebrew Diary of a CEO", a Hebrew video podcast of about an hour per episode that interviews Israeli cybersecurity CEOs and founders. It is recorded at the RHEL Guts Innovation Hub. We want the views and viral short clips that The Diary of a CEO (Steven Bartlett) and the Jack Neel Podcast get.

This repo holds the research, the principles and the per-guest prep that the production team and the host use before each recording. There is no code here.

## Language

All deliverable files are in Hebrew, because the podcast is in Hebrew. CLAUDE.md and the README are in English. Research can be done in either language. Company names, podcast names and clip titles keep their original spelling (Armis, The Diary of a CEO). In the Hebrew files, no line, heading, bullet, sentence or source entry starts with an English letter or with a link. A line that opens with an English word or a link is laid out left to right, which breaks the right-to-left alignment of the whole list. This applies even when the bullet is only a link, including Hebrew-titled links: write "בכלכליסט: [title](url)", never "[כלכליסט, title](url)". Digits are fine ("2019: ..."). When the subject is an English name or a link, open with a Hebrew word and put the name after it: "בקליף [DOAC, ...](url)", "לפי [Chris Chow](url)", "ב-ynet: [title](url)", "חברת Armis הודיעה", "לדעתך, AI יחסל...". Spell "קליפ" and "קליפים" with פ, never "קליף". Write view, subscriber and download counts as 814k, 2.3M or 100M, never "814 אלף צפיות" or "2.3 מיליון צפיות". Foreign place names are written in English and always followed by the country. If the name or the country has changed, give both the historical and the current form, for example "Dnipropetrovsk שבברית המועצות (היום Dnipro, אוקראינה)".

## Files

- `01-interviewers-and-principles.md`: a static reference work about five interviewers (Bartlett, Neel, Stebbings, the Acquired hosts, Rhysider) and their interview principles. It never mentions our podcast, our team, our episodes or a specific guest; examples are generic. Each interviewer gets a short prose profile of who he is and what he does, then a numbered list of principles with no links, then the heading "### יישום העקרונות" followed by a numbered list in which item N demonstrates principle N with a real YouTube Short, quoting what is said in it. The principles list has no heading of its own. The file closes with general sections on preparation and on the studio.
- `02-<guest>-guest-data.md`: static facts about the guest, written entirely as short, specific bullet points with dates and numbers and no prose paragraphs. Sections: basics, childhood, military and education, career, the company in numbers, "ציטוטים מהעבר", comparison with another CEO, pop culture, previous interviews, sources. "ציטוטים מהעבר" holds exactly the 10 most interesting and relevant quotes from the guest, one per item, each followed by its source and date. Current file: `02-nadir-izrael-guest-data.md`.
- `03-<guest>-questions.md`: bullet points of questions only, grouped by act, with follow-ups nested under them. After the questions comes the pre-show checklist for that guest. Current file: `03-nadir-izrael-questions.md`.
- `04-editing-principles.md`: editing principles in the same format as 01: a principles list, then "### יישום העקרונות" and the demonstrations. Covers short clips, titles, the full episode and trailer, thumbnails and distribution.

## Evidence and links

Every principle in 01 and 04 needs a demonstration. Use a real YouTube Short (never TikTok) from one of the five model podcasts, and say exactly what happens in it, preferably quoting the host's question or the clip's first line. When no Short can show the principle (silence, research habits, thumbnail tests), cite the article it comes from instead. Use verified URLs only.

Real Shorts with view counts come from a channel's YouTube RSS feed. Popular Shorts: `https://www.youtube.com/feeds/videos.xml?playlist_id=UUPS<channel id without "UC">`. Latest uploads: `?channel_id=<id>`. Channel IDs:

- DOAC `UCGq-a57w-aPwyi3pW7XLiHw`
- DOAC Clips `UCnjgxChqYYnyoqO4k_Q1d6Q`
- Jack Neel `UCFRCiFkWWJN2rO6dsKU9-1A`
- 20VC `UCf0PBRjhf0rF8fWBIxTuoWA`
- Acquired `UCyFqFYfTW2VoIQKylJ04Rtw`
- Darknet Diaries Clips `UCXnxYgJ52Jwx9LAa-ARWjEg`

Transcripts can be pulled with the `youtube-transcript-api` Python package. YouTube blocks the IP (`IpBlocked`) if you fetch fast, so leave several seconds between requests.

List sources at the end of each file. Attribute secondhand figures in the sentence itself (for example "לפי ynet").

## Final, polished files

Every file is a finished document ready to hand to the team. That means:

- No metadata or intro lines about the file, who it is for or how to read it.
- No references to other files in the repo, whether by name, number or link.
- No verification markers such as ⚠️ or "(לאמת)". Use only guest facts that have a named source, and attribute them in the sentence ("לפי ynet").
- No placeholders, drafts or notes to ourselves.

## Length and tone

Write short. A principle is a general rule that says what to do and when. Principles are general and never about one specific topic such as money. "שאלה על הצלחה מנסחים דרך ההשפעה שלה על האנשים הקרובים לאורח" is right, and "שאלה על כסף..." is wrong. A demonstration can still be a clip about money. It contains no example: no sample question, quote or wording. Examples belong only in the demonstration list that follows, and each demonstration is a real clip or source. Leave out explanations of why something works and any intro about what the document is. The questions file can be long because it has to fill an hour plus backups.

## Writing that does not read as AI-generated

These are the most common tells of AI-written text, compiled from Wikipedia's "Signs of AI writing" guide and Pangram's frequency data. None of them should appear in any file in this repo, Hebrew or English.

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
20. Templated parallel sections: every section ending with the same formula, such as "we learn X from him because Y" followed by "we don't take Z because W". Leave out the closing line rather than repeat a formula.
21. Unverifiable content: invented or broken links, placeholders (XX, "INSERT"), or claims that can't be traced to a source.

## Question-writing rules (03)

Structure:

- The file holds only bullet points of questions, grouped by act, with follow-ups nested under the main question. Nothing else comes before the checklist.
- The order follows the DOAC arc: an opening hook, childhood, the road, the peak and what it cost, cyber and AI, Israel, a speed round, and the closing ritual (the guest answers a question left by the previous guest and writes one for the next).
- One question per line. Never a double question ("שאלה כפולה"), meaning two questions in one sentence, such as "What did you learn at Google, and how did it shape Armis?". The guest answers one half and the answer can't be clipped. Ask the main question, then each follow-up separately. Whenever a file mentions a double question, explain what it is.

Length:

- The question itself is about 12 words. With context it is at most one short sentence of context plus the question, about 25 words in total.
- Give only the facts the question needs: one or two numbers and a date. Skip the round size, quotes and backstory unless the question is about them.

Wording:

- Every question, including the speed round, is a full question that spells out what is asked. Either/or questions name both options in full ("לעבוד בגוגל או לעבוד בסטארטאפ?" and never "גוגל או סטארטאפ?"). No shorthand and no bare noun phrases.
- Closed questions are natural questions ("נעלבת?"), never prefixed with "כן או לא:".
- Use the professional terms of the Israeli cyber industry (אבטחת IoT, OT, CISO, ניהול חשיפה, סבב גיוס, הנפקה), not lay descriptions such as "חברות שאבטחו מכשירים מחוברים". For financial mechanics that aren't the point, say what happened in plain words: "הדירקטוריון לא רצה אותם כמשקיעים", not "התנגד בגלל הדילול".

Facts:

- When a question rests on events, state them with their exact dates and figures, then ask what happened between them. Don't make the guest work out a timeline, and never ask a vague "how long after...".
- Check who actually said each thing. If the co-founder said it, write "you said" in the plural or name him.
- Look up every date and figure before using it. Don't invent exact numbers we can't source, such as "עשרות חברות". A general framing is fine: "לא מעט סטארטאפים שנכשלו".
- The context must state the contrast that gives the question its point. If we ask what the guest did differently, the context says what happened to the others ("שנכשלו"). Without it the question has no tension and the guest has nothing to answer against.
- Every quote names its source and date. Every person is introduced on first use ("יבגני דיברוב, השותף שלך").

Standing on its own:

- The file must make sense to someone who hasn't read any other file. The questions stay short, and the stage directions carry the detail.
- Stage directions are only for actions that need setup: showing a clip, bringing out a prop, the closing ritual. Never add interviewing-technique cues such as silences, pauses or "reflect back", in any form ("(שתיקה)", "(שותקים חמש שניות...)"). Technique belongs in the principles file, not in the questions. Stage directions go in parentheses and spell out exactly what to do. For a clip: which show, channel, year and character, what happens in it, how long it runs, what to film, the rights needed, and the fallback. For a prop: what it is, where it comes from, and when to bring it out.
- When a question rests on a fact the interviewers might find confusing or think is wrong, put a note for the interviewer before it: "(הסבר למראיין: ...)". This covers things like a company sold twice, a co-founder being the one who said something, or a figure that contradicts common knowledge. The note says what happened, with dates and figures, and which event the question is about. The interviewer reads it; it is not said out loud.

Focus:

- A confrontation question uses one past quote, one fact that contradicts it, and one question, for example "ב-2021 אמרת X. ב-2025 עשיתם Y. מה השתנה?". Don't stack two quotes on one topic, don't add a permission line ("אפשר לחלוק עליך?") in front of it, and don't follow up with a summary that puts words in the guest's mouth ("אז מה שאתה אומר זה ש...").
- Each main question explores one idea. Follow-ups dig deeper into that same idea and never open a new one.
- Every question has one clear thing to answer. Avoid vague "what did you see" or "what did you feel when you walked in" prompts that only hint at an intended answer. Ask the concrete thing directly ("מה סיפרת להם?").
- Ask what the guest knows from his own work, not for speculation. Avoid sensational "how close are we to disaster" questions that he can only answer with a guess ("כמה קרובים אנחנו לבית חולים מושבת?"). Ask something concrete that his experience lets him answer ("איזו מערכת בישראל הכי חשופה היום?").
- A follow-up says explicitly what it refers to ("גם בחמישה מיליון האלה"). The interviewer should never have to guess which event, number or quote it points back to.

Closing section:

- At most four lines: a legacy question, the emotional question (here, the letter to his mother), the previous guest's question, and the question he leaves for the next guest.
- The legacy question is concrete and personal ("מה אתה רוצה שיגידו עליך בעוד עשרים שנה?"). Avoid grandiose prompts like "מה המסר שלך לעולם?", which get platitudes.
- The ritual stage direction is one short sentence and covers the case where there is no previous guest. The question for the next guest is a plain question on its own line.

Respect:

- Every question is respectful. Never ask about the guest's personal wealth, how much he personally made, what he bought, or whether a reported sum is true. The most we ask is what the exit did or did not change in his life. Company figures (rounds, valuations, deal price) are fine.

Techniques:

- Use the techniques from 01: an opener with a number; warm questions before hard ones; "take me to that moment" (Rhysider); a best-ever question followed by "how much?" about company figures (Stebbings); closed and agree/disagree questions (Neel); a past quote set against what happened later (Bartlett); comparing him with another CEO (Stebbings); a prediction with a year (Bartlett); "explain it to my mom"; "say that in one sentence"; a game (Neel); a legacy question.
- Before writing, listen to and read the guest's previous interviews in Hebrew and English. Skip questions he has already answered and go further than those interviews did.

## Pre-show checklist (end of 03)

The checklist lists only the sensitive topics we have to clear with the guest before recording, phrased as what we ask him ("האם מותר לשאול על...?"). Rules:

- Unnumbered bullet points, no more than 10.
- Only topics that one of the questions actually touches, such as family, military service (military censorship), the co-founder relationship, deal details, the acquirer as a public company, specific attacks or state actors, satire about the guest, or living abroad. Pick the 10 that matter most for this guest.
- Nothing else goes in the checklist: no format explanations, answer guidelines, legal or PR items, fact-checks, props, logistics or distribution. It never mentions other podcasts or how we position our show.

## Current guest

Nadir Izrael (נדיר יזרעאל), co-founder and CTO of Armis. ServiceNow bought Armis for $7.75B; the deal was signed in December 2025 and closed in April 2026. He grew up in Kiryat Ata. His mother was disabled in a car accident before he was born. He went to a yeshiva high school, served in Unit 8200, studied at the Technion and worked at Google. The Eretz Nehederet character "Nadir Ackerman" is named after him. See `02-nadir-izrael-guest-data.md` and `03-nadir-izrael-questions.md`.
