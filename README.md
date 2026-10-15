# On the Spot

A rehearsal game for memorizing a talk, hosted by two cats. Paste your script, and the cats quiz you: you get the opening words of a passage, say the rest out loud, and submit. They help you notice when you've got the general idea, the exact words, or need to read that part and try again.

It runs entirely in your browser as a single file. Your talk is never uploaded, and it is not saved unless you ask: it is held in memory for the visit only, and the next visit (or a reload) starts empty, so you paste it again. At the end of a round the cats offer "Remember me on this computer", which keeps the talk and your rough spots in that browser on that device (and nowhere else); "Forget me", "Start over", or simply closing the tab wipes it. The page has a **Privacy** card that explains, in plain language, exactly what happens and what the optional outside connections are (the browser's own speech-to-text for the mic button, the Word/PDF readers fetched on demand, and Claude judging if someone adds an API key).

## Use it

1. Open the page (your GitHub Pages link, or `index.html` in Chrome).
2. Paste your talk (or press "Try a sample" to play a round with a short public-domain speech first). Blank lines separate sections. A line starting with `#` names the section that follows it. Stage notes in [brackets] (a breath mark, a cross, a prop) are shown with the line and never counted as words, so you can rehearse the move with the line. Pick how to split sections into prompts (every 1–3 sentences, or one prompt per line if you want to control the breaks yourself).
3. Start a round. The plans come in two groups.
   - **The whole talk.** *Guided run* (training), in parts of about five minutes: say the talk; if you stop for 3 seconds, what you've said locks in and the line you're standing in front of appears, so you read it and keep going instead of rehearsing a blank. At the end you can drill the passages where you paused, or the handoffs into them. At the end of each part the whisper reports how it went (lines flowed, pauses) and offers Keep going or Review this part first; a review mid-run ends with Continue the run, which picks up at the line you stopped on. A skip is handled by its size: one line left out inside a beat is noted in the whisper and you keep going; a beat skipped rewinds you to the last line that went right, with the skipped lines shown; a whole part (or six-plus lines) left out shows only its first words, with Back to its cue or Carry on, drill it after, and gets its own pattern (Skipped a part). Three pauses within three beats mid-run, and the whisper offers to stop there, smooth out just those beats, and pick the run back up at the line where you stopped. *Test run* (testing): say the whole talk with no help, then see what you left out. *Rehearse cycle* (the default): a guided run, then four short rounds on exactly the spots where you paused and the handoffs around them, then Build up takes over.
   - **The whisper, everywhere.** Any prompt of two beats or more (a one-minute run, a Smooth out step, the whole talk from a cue) runs through the same prompter as a Guided run, scoped to the passage: pause and the next line is whispered, jump ahead and the game rewinds you to the last line that went right, and everything you said is graded as one answer at the end. In a long passage every swap and every missed line is marked in place, and the offer is to smooth out those spots, never to redo the whole passage for one word. A Customize knob makes the whisper apply to every prompt, or to none; Test run never whispers.
   - **Comfort sheet.** A printable landscape page of your cues: the first three words of every beat, in order, by part, with the spots you've missed starred, stage notes inline, and the key terms in order of first use. The same cues you've been retrieving from, so they work on stage. Also copies as plain text for a comfort slide.
   - **Handoffs.** Every seam between beats as a round: the tail of one beat is the cue, you say the next. Changes between parts of the talk come first, then the rest, favoring what you've missed. In a Guided run, a shown line that opens a beat or a part is labeled as a handoff or part change, and "Back up" after a jump returns you to the last line that went right so the seam is rehearsed, not just the line.
   - **Listen.** A warm-up: the device's own voices read the talk (or just your trouble spots, or the last stretch) at 1×–2×, each word lit as it's spoken. Voices: a different main voice each passage, any one main voice by name, or, for fun, the computer's weirdest voices in rotation or a cast of characters with pitches and speeds all over the place. Nothing is sent anywhere. It ends by offering a Guided run or Test run, because hearing it is review and saying it is the rep.
   - **Smooth out.** After any run with misses or pauses, the review offers a ladder for exactly those spots: the lines around each one (the line before as the cue, say the missed line and the next), then two beats, then a bigger run of about a minute, then the whole talk again. More than three spots, and it starts with each one on its own. A missed line in a long run is shown in place with its neighbors; you are never sent back to the top for one line.
   - **Practice plan.** The review names what went wrong at each rough spot and runs the matching sequence: *Handoff stall* (you had the beat, then stopped at the seam), *Dropped line*, *Beat jump* (you left one beat and landed in a later one), *Order inside the beat*, *Wording drift* (the idea without the words, more than once), *Cold cue* (the opening words brought nothing back), *Sticky spot* (missed in three or more runs). The table of patterns and sequences is in the page itself; nothing is sent anywhere and no AI is involved at play time.
   - **Bibliography.** A footer link opens the bibliography of memorization techniques used in the game (playful learning, errorless learning and prompt fading, retrieval and spacing research, speech coaches), with a note on what each source gave the game.
   - **Trouble spots.** The start screen shows which passages keep being missed or paused on, with the recent runs, and buttons to smooth out or drill them. This history is held for the visit, or kept on that computer with "Remember me".
   - **In pieces.** *Mixed passages* (one passage at a time, shuffled), *Begin with the end* (the last stretch only), *Build up* (single passages → transitions → one-minute runs → three-minute runs → the whole talk from a cue), and *Customize* (pick parts, length, number of prompts, opening words, pick order, hints). "What the knobs do" at the top of the page has the cats explaining each one.
Every prompt's cue is whispered the same way, by the tabby peeking from the wings: "Psst. It starts:" and the opening words, "and then?" for a handoff. One visual language from the first prompt to the full run.

4. Talk. Chrome and Edge give you a live mic button (it starts listening on each prompt; turn that off in settings if you'd rather tap). Safari and Firefox don't support in-page speech recognition, so use your keyboard's microphone to dictate instead (Mac: the Dictation shortcut; iPhone/iPad: the mic on the keyboard; Windows: Win+H). The mic can listen for a full talk in one go.
5. Submit (or ⌘/Ctrl-Enter). Stop at a beat and the cats ask you to keep going instead of marking you wrong; say things out of order or skip a part, and they tell you which. Keep going past the passage and all of it is graded, with the line that follows what you actually said shown next. At the end you get a review, an award, the cats' nap, and the choice to be remembered or forgotten.

Every plan favors what you've missed: passages you've stumbled on come back more often. Nothing marks a passage as "wrong" in the lists; you only ever see the correct version to practice. Small edits to your script keep your progress; the passages that changed simply start fresh.

## Characters and key terms

When you paste a script, the setup page guesses its characters and names (capitalized names, and role words that speak or act: the guard, the captain) and its key terms (the content words the talk leans on), from the text alone, with no AI. Edit both lists freely. Saying the wrong one of these ("the captain" where the line says "the guard", a number, a negation, or a term you don't introduce until later) is a miss: the wrong word is struck out, the right one is bright, and a cat asks you to read the whole passage again before you say it again. It also gets its own practice pattern (Word swap), and a wrong character is named as such.

Three built-in checks also count as a miss unless you turn them off on the setup page: a changed number, a dropped or added negation (not, never, no), and a term said before the talk introduces it. When one of these counts against you, the screen says which rule did it and offers one tap to score swaps like that as correct from then on, with the new rule spelled out.

Any other swapped word is, by default, close enough: "said" for "replied" is a wording note, the passage counts, and the game asks right there whether that word matters. One tap adds it to your key terms, and from then on it counts as a miss. Switch "every word" on the setup page if any swapped word should count.

## How it judges

By default, a word-by-word comparison with your script, on your computer. It forgives filler words, contractions, typos and speech-to-text slips (including "30" for "thirty"), sentences said in a different order, and extra words if you run on into the next passage. It stops you when a whole sentence or idea is missing or a number is wrong. Natural rewordings that keep the idea pass with a wording note.

**Optional: let Claude judge meaning.** Open "Judging" on the start screen and paste an Anthropic API key. Then Claude decides whether what you said is "basically the same," lists small tweaks, and names anything missing. The key is stored only in your browser and sent only to `api.anthropic.com`; usage is billed to that key. Get a key at https://console.anthropic.com.

## What it needs

An ordinary, steady internet connection: the page loads once (about 4 MB, for the cat clips), and after that only the mic button talks to the network, because Chrome and Edge do their speech-to-text online. Typing or dictating with the keyboard works offline once the page is open. In-page mic: Chrome or Edge on a computer or Android; on iPhone and iPad, use the keyboard mic.

## Put it on GitHub Pages (free, about two minutes)

1. Create a new repository on GitHub (public is fine; the page holds no talk, ever).
2. Upload `index.html` and this `README.md`.
3. In the repository, open **Settings → Pages**, set the source to **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
4. After a minute your page is live at `https://<your-username>.github.io/<repository-name>/`. Share that link with other speakers; each person pastes their own talk, and it stays in their own browser.

To update: upload a new `index.html` over the old one (GitHub asks you to commit the change). Anyone who already has the page open sees a "new version" pill within a few minutes and can reload with one tap; nobody's script is affected, because scripts are never in the page.

A hosted page also fixes one Chrome annoyance: a file opened from disk asks for microphone permission on every listen, while a real web address remembers "Allow while visiting the site."

## Credits

Made by Erica Key of Learning Seeds for her TEDx talk and for fellow speakers, with errorless-learning habits: retrieval first, the correct version shown only when needed, and no marks on what went wrong.
