# On the Spot

A rehearsal game for memorizing a talk, hosted by two cats. Paste your script, and the cats quiz you: you get the opening words of a passage, say the rest out loud, and submit. They help you notice when you've got the general idea, the exact words, or need to read that part and try again.

It runs entirely in your browser as a single file. Your talk is never uploaded, and it is not saved unless you ask: it is held in memory for the visit only, and the next visit (or a reload) starts empty, so you paste it again. At the end of a round the cats offer "Remember me on this computer", which keeps the talk and your rough spots in that browser on that device (and nowhere else); "Forget me", "Start over", or simply closing the tab wipes it. The page has a **Privacy** card that explains, in plain language, exactly what happens and what the optional outside connections are (the browser's own speech-to-text for the mic button, the Word/PDF readers fetched on demand, and Claude judging if someone adds an API key).

## Use it

1. Open the page (your GitHub Pages link, or `index.html` in Chrome).
2. Paste your talk (or press "Try a sample" to play a round with a short public-domain speech first). Blank lines separate sections. A line starting with `#` names the section that follows it. Pick how to split sections into prompts (every 1–3 sentences, or one prompt per line if you want to control the breaks yourself).
3. Start a round. The default plan is **Rehearse**: you say the whole talk from the top without stopping, the cats note what you skipped, and the next four short rounds drill exactly those passages and the handoffs into and out of them. After that the plan moves on to **Build up** (single passages → transitions → one-minute runs → three-minute runs → the whole talk from a cue). Other plans: **Begin with the end**, **Whole talk**, **Full run**, and **Customize** (pick parts, length, number of prompts, opening words, pick order, hints). "What the knobs do" at the top of the page has the cats explaining each one.
4. Talk. Chrome and Edge give you a live mic button (it starts listening on each prompt; turn that off in settings if you'd rather tap). Safari and Firefox don't support in-page speech recognition, so use your keyboard's microphone to dictate instead (Mac: the Dictation shortcut; iPhone/iPad: the mic on the keyboard; Windows: Win+H). The mic can listen for a full talk in one go.
5. Submit (or ⌘/Ctrl-Enter). Stop at a beat and the cats ask you to keep going instead of marking you wrong; say things out of order, skip a part, or say more than asked, and they tell you which. At the end you get a review, an award, the cats' nap, and the choice to be remembered or forgotten.

Every plan favors what you've missed: passages you've stumbled on come back more often. Nothing marks a passage as "wrong" in the lists; you only ever see the correct version to practice. Small edits to your script keep your progress; the passages that changed simply start fresh.

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
