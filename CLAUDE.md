# CLAUDE.md

## What this project is

We are building "the Hebrew Diary of a CEO", a Hebrew video podcast of about an hour per episode that interviews Israeli tech founders and CEOs, many of them from cybersecurity. It is recorded at the RHEL Guts Innovation Hub. We want the views and viral short clips that The Diary of a CEO (Steven Bartlett) and the Jack Neel Podcast get.

This repo holds the research, the principles and the per-guest prep that the production team and the host use before each recording. There is no code here.

## Language

All deliverable files are in Hebrew, because the podcast is in Hebrew. CLAUDE.md and the README are in English. Research can be done in either language. Company names, podcast names and clip titles keep their original spelling (Armis, The Diary of a CEO). In the Hebrew files, no line, heading, bullet, sentence or source entry starts with an English letter or with a link. A line that opens with an English word or a link is laid out left to right, which breaks the right-to-left alignment of the whole list. This applies even when the bullet is only a link, including Hebrew-titled links: write "בכלכליסט: [title](url)", never "[כלכליסט, title](url)". Digits are fine ("2019: ..."). When the subject is an English name or a link, open with a Hebrew word and put the name after it: "בקליף [DOAC, ...](url)", "לפי [Chris Chow](url)", "ב-ynet: [title](url)", "חברת Armis הודיעה", "לדעתך, AI יחסל...". Spell "קליפ" and "קליפים" with פ, never "קליף". Write view, subscriber and download counts as 814k, 2.3M or 100M, never "814 אלף צפיות" or "2.3 מיליון צפיות". Foreign place names are written in English and always followed by the country. If the name or the country has changed, give both the historical and the current form, for example "Dnipropetrovsk שבברית המועצות (היום Dnipro, אוקראינה)".

## Preparing questions for a new guest

When the user asks for questions for a new guest, do all of this without being asked:

1. Create the folder `<guest-slug>/` with `<guest-slug>-guest-data.md`, `<guest-slug>-questions.md` and `<guest-slug>-intro.md`.
2. Research the guest in depth, in Hebrew and English. Search news and press archives (Globes, Calcalist, TheMarker, ynet, Geektime and the English-language tech press) and the company's announcements. Make sure each item is about this guest and not someone with the same name.
3. Find every previous interview: podcasts, YouTube videos and conference talks. Pull the YouTube transcripts with `youtube-transcript-api` (Hebrew captions are `iw`), a few seconds apart. Extract passages by keyword (childhood, parents, partner, children, the army, each company, money offers, crises, the board, leaving, book, sport, regrets) and read them. These transcripts hold the personal moments that make the best questions.
4. Write the guest-data file from what you verified.
5. Write the questions following the rules in this file and the playbook.
6. Run every question through `principles/question-qa.md`: the 20 boxes, then the 50 checks, comparing against the before/after examples. Then score it against the ten-point rubric in `principles/interviewer-playbook.md`. A question is final only when it passes both. Rewrite or cut any question that fails a point. Pay particular attention to questions he has already answered in earlier interviews, hidden assumptions, context a stranger wouldn't understand, and literary or clever phrasing.
7. Write the intro narration following `principles/intro-principles.md`, using only facts from the guest-data file. Check every line against each principle in that file and rewrite any line that fails one.
8. Check all three files against `AI-WRITING-DONTS.md` before handing them over.
9. Add the guest to the "Guests" section of this file.

## Files

File names carry no numbers.

- `AI-WRITING-DONTS.md`: the 30 things that make text read as AI-generated. Read it before writing or editing any file, and check every file against it before handing it over.
- `principles/interviewers-and-principles.md`: a static reference work about five interviewers (Bartlett, Neel, Stebbings, the Acquired hosts, Rhysider) and their interview principles. It never mentions our podcast, our team, our episodes or a specific guest; examples are generic. Each interviewer gets a short prose profile of who he is and what he does. The profile's first paragraph ends with one plain sentence, with no label, on the idea that guides his show, taken from his own words or a sourced description. After the profile comes a numbered list of principles with no links, then the heading "### יישום העקרונות" followed by a numbered list in which item N demonstrates principle N with a real YouTube Short, quoting what is said in it. The principles list has no heading of its own. The file closes with general sections on preparation and on the studio.
- `principles/interviewer-playbook.md` (English): how the five interviewers actually ask questions, taken from their own transcripts, with the examples most relevant to Israeli founders, and the ten-point rubric that every question must pass.
- `principles/question-qa.md` (English, with Hebrew examples): the 20-box final check every question must pass, 50 concrete checks for critiquing a question, and real before/after edits from this project with the reason for each. Every time the user asks to revise a question, add that edit to part 3 (before, after, why) and, if it shows a new kind of mistake, add a check to part 2. The file only grows: never delete or shorten an existing check or example, even when a later edit supersedes it. Part 3 keeps growing up to 500 examples; number new entries after the last one.
- `principles/editing-principles.md`: editing principles in the same format: a principles list, then "### יישום העקרונות" and the demonstrations. Covers short clips, titles, the full episode and trailer, thumbnails and distribution.
- `principles/intro-principles.md`: principles for the narrated intro at the start of an episode, where the host introduces the guest in up to a minute of narration cut between clips from the episode. Same format as the editing principles: a principles list, then "### יישום העקרונות" and the demonstrations.
- `<guest-slug>/<guest-slug>-guest-data.md`: static facts about the guest, written entirely as short, specific bullet points with dates and numbers and no prose paragraphs. Typical sections: basics, childhood, before tech or military, one section per company, after the company, media about him (a satire character, a book, a series), "ציטוטים מהעבר", comparison with another CEO, previous interviews, sources. "ציטוטים מהעבר" holds exactly the 10 most interesting and relevant quotes from the guest, one per item, each followed by its source and date.
- `<guest-slug>/<guest-slug>-questions.md`: bullet points of questions only, grouped by section, with follow-ups nested under them. No title line, no stage directions, no interviewer notes, no backup section and no checklist. The file is only what the interviewer asks out loud.
- `<guest-slug>/<guest-slug>-intro.md`: the narration the host records for the episode intro, written before the recording from the guest-data file. Four to six lines of narration as a numbered list, about 30 to 60 seconds read aloud: an opening hook with a number or a strong claim about the guest, then one fact per line in the order of his life, then a line on what the viewer will find out in the episode, and his name last. The file holds only the lines the host reads out loud, followed by the sources for its facts. No clip slots, stage directions or notes. After the recording, the lines are updated to fit the clips chosen for the trailer.

Each guest has his own folder (`nadir-izrael/`, `raanan-cohen/`) holding his guest-data, questions and intro files. The principles files live in `principles/` because they apply to every guest.

## Evidence and links

Every principle in the principles files needs a demonstration. Use a real YouTube Short (never TikTok) from one of the five model podcasts, and say exactly what happens in it, preferably quoting the host's question or the clip's first line. When no Short can show the principle (silence, research habits, thumbnail tests), cite the article it comes from instead. Intro principles are demonstrated with the opening minutes of a real full episode, quoted from its transcript, because Shorts don't include the intro. Use verified URLs only.

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

Follow `AI-WRITING-DONTS.md` in every file, Hebrew or English. When a file breaks one of its rules, fix it, and add any new tell the user points out to that file.

## Question-writing rules (questions files)

Structure:

- The file holds only bullet points of questions, grouped by act, with follow-ups nested under the main question. Nothing else goes in the file.
- Sections follow the guest's life in order: an opening, childhood, how he got into tech, each company, the turning point (an exit, a sale or a departure), what he does now (his field, a book, a sport), Israel, a speed round, and the closing. Name each section after the actual period or event in plain words: "ילדות", "החברה הראשונה", "העזיבה", "הספר". Never use abstract "X ו-Y" titles such as "הפסגה והמחיר" or wordplay such as "הילד מקריית אתא". The Israel section and the section on his field are short: two to four questions each.
- Bold exactly one question in the whole file: the central question of the episode.
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
- The context must explain itself. A viewer who knows nothing about the guest must understand from the question alone why the detail matters and what is being asked. Never open with a cryptic fragment of backstory ("ביום חמישי יש אצלכם ערב פיצה") and leave the link unstated. Say the link outright ("הרעיון ל-Bringg נולד מפיצה שהזמנתם הביתה ואיחרה"), then ask. Test every question by reading it as a stranger would.
- Don't cross-examine. Most questions should be open ("איך...?", "ספר לי...") with no premise at all. Use one short, neutral premise only when the question makes no sense without it, avoid stacking "אמרת ש..." statements, and never tell the guest his own punchline before he says it. A pile of facts about him before the question sounds like an attack.
- No hidden assumptions. A question may only presuppose a feeling, event or opinion the guest has stated publicly. Otherwise ask openly. "מתי הרגשת שזה גדול עליך?" assumes he felt out of his depth; ask "איך הרגשת ביום ההנפקה?" instead. Before finalizing, check every question for words like "מתי", "למה", "מה הכי" or "איך התמודדת" that take something for granted, and confirm a source for each.
- Every quote names its source and date. Every person is introduced on first use ("יבגני דיברוב, השותף שלך").

Standing on its own:

- The file must make sense to someone who hasn't read any other file. Every question carries its own context: dates, figures and names inside the question itself.
- No stage directions, props, clips or interviewer notes in the questions file. If a question needs background to be understood, put that background into the question in one short sentence, or drop the question.

Closing section:

- Three questions: a general question on how the guest's achievement changed the way he looks at life (phrased generally, without the sale price or company name), "אם זה הראיון האחרון שלך, מה המסר שלך לעולם?", and "מה אתה רוצה שיגידו עליך בעוד עשרים שנה?".

Respect:

- Every question is respectful. Never ask about the guest's personal wealth, how much he personally made, what he bought, or whether a reported sum is true. The most we ask is what the exit did or did not change in his life. Company figures (rounds, valuations, deal price) are fine.

Techniques:

- Use the techniques from the interviewer principles: an opener with a number; warm questions before hard ones; "take me to that moment" (Rhysider); a best-ever question followed by "how much?" about company figures (Stebbings); closed and agree/disagree questions (Neel); a past quote set against what happened later (Bartlett); comparing him with another CEO (Stebbings); a prediction with a year (Bartlett); "explain it to my mom"; "say that in one sentence"; a game (Neel); a legacy question.
- Before writing, listen to and read the guest's previous interviews in Hebrew and English. Skip questions he has already answered and go further than those interviews did.

## Guests

- `nadir-izrael/`: Nadir Izrael (נדיר יזרעאל), co-founder and CTO of Armis. ServiceNow bought Armis for $7.75B; the deal was signed in December 2025 and closed in April 2026. He grew up in Kiryat Ata, went to a yeshiva high school, served in Unit 8200, studied at the Technion and worked at Google. The Eretz Nehederet character "Nadir Ackerman" is named after him.
- `raanan-cohen/`: Ra'anan Cohen (רענן כהן), "Unicorn & IPO Founder". He founded MobileMax (IPO on the Tel Aviv Stock Exchange in June 2007, collapsed after 2008) and co-founded Bringg (CEO 2013 to July 2018; $1B valuation in June 2021). He wrote the novel "רק עוד קצת ודי", which is being adapted for TV, and runs ultramarathons. He is a different person from Ra'anan Cohen the former Labor minister; don't mix their press coverage.
- `boris-vaynberg/`: Boris Vaynberg (בוריס ויינברג), co-founder and CEO of Blast Security (cloud security, $10M seed from 10D and MizMaa in November 2025). He immigrated from Kishinev (today Chișinău, Moldova) at 8, served about eight to nine years in Mamram, worked at Comsec and Elbit, and co-founded Solebit, sold to Mimecast in July 2018 for about $88M. He ran Mimecast Israel until after the Permira buyout (May 2022), and the idea for Blast came during his reserve duty after October 7. The press spells his name Vaynberg, Vineberg, Weinberg or ויינברג. He is a different person from the Boris Vaynberg who runs Venus Concept seminars.
- `michael-dolinsky/`: Michael Dolinsky (מיכאל דולינסקי), co-founder and CTO of Ermetic (cloud security, founded July 2019), sold to Tenable for $265M (announced September 2023, closed 2 October 2023) and now Tenable Cloud Security, where he is CTO. He grew up in Netanya, went through the Mamram programming course and served seven years in Matzov (2001 to 2008), then worked five years at Microsoft Israel. He co-founded Aorato with Idan and Ohad Plotnik at the end of 2012; Microsoft bought it in November 2014 for a reported $200M and built ATA on it, and he stayed about three and a half years. He is an angel investor (Solebit, Panorays, Fabrix Security) and a close friend of Boris Vaynberg. His only long earlier interview is the MamraMic podcast (June 2020), which is audio only, so it was transcribed with Whisper. Several unrelated Michael Dolinskys appear in US results; don't mix them up.
