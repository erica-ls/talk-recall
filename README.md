# Talk Recall

A retrieval drill for memorizing a talk **out of order**. You get the opening words of a passage from anywhere in your talk, say the rest out loud, and submit. If it's basically the script, you move on. Small wording differences wait for a review at the end of the round. If you leave out a sentence or an idea, you hear about it right away, see the passage once, and say it again.

It runs entirely in your browser as a single file. Your talk is saved only in that browser, on that device, and is never uploaded. The page has an **Privacy** card that explains, in plain language, exactly what stays local and what the two optional outside connections are (the browser's own speech-to-text for the mic button, and Claude judging if someone adds an API key).

## Use it

1. Open the page (your GitHub Pages link, or `index.html` in Chrome).
2. Paste your talk. Blank lines separate sections. A line starting with `#` names the section that follows it. Pick how to split sections into prompts (every 1–3 sentences, or one prompt per line if you want to control the breaks yourself).
3. Start a round. Choose which sections, how many prompts, how long each prompt runs (one passage, several, or to the end of the section), how many opening words you get, and whether to show where to stop.
4. Talk. Chrome and Edge give you a live mic button (it starts listening on each prompt; turn that off in settings if you'd rather tap). Safari and Firefox don't support in-page speech recognition, so use your keyboard's microphone to dictate instead (Mac: the Dictation shortcut; iPhone/iPad: the mic on the keyboard; Windows: Win+H).
5. Submit (or ⌘/Ctrl-Enter). Read the result, keep going. At the end you get a review and a "Run those again" button.

Your talk, settings, and progress stay in that browser (localStorage). "Favor what I've missed" uses your history to pick passages you've stumbled on more often. Nothing marks a passage as "wrong" in the lists; you only ever see the correct version to practice.

## How it judges

By default, a word-by-word comparison with your script, on your computer. It forgives filler words, contractions, typos and speech-to-text slips (including "30" for "thirty"), and extra words if you run on into the next passage. It stops you when a whole sentence or idea is missing or a number is wrong. Natural rewordings that keep the idea pass with a wording note.

**Optional: let Claude judge meaning.** Open "Judging" on the start screen and paste an Anthropic API key. Then Claude decides whether what you said is "basically the same," lists small tweaks, and names anything missing. The key is stored only in your browser and sent only to `api.anthropic.com`; usage is billed to that key. Get a key at https://console.anthropic.com.

## Put it on GitHub Pages (free, about two minutes)

1. Create a new repository on GitHub (public is fine; the page holds no talk until someone pastes one).
2. Upload `index.html` and this `README.md`.
3. In the repository, open **Settings → Pages**, set the source to **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
4. After a minute your page is live at `https://<your-username>.github.io/<repository-name>/`. Share that link with other speakers; each person pastes their own talk, and it stays in their own browser.

A hosted page also fixes one Chrome annoyance: a file opened from disk asks for microphone permission on every listen, while a real web address remembers "Allow while visiting the site."

## Ship it with a talk preloaded

To hand someone a copy that opens straight into their talk, add this before the main `<script>` in `index.html`:

```html
<script>
window.DEFAULT_TALK = {
  name: "TEDx Somewhere · Nov 3",        // shown above the title
  appName: "My Talk Recall",             // the page title
  split: "line",                         // "line", "1", "2" or "3"
  text: "# Opening\nFirst passage on one line.\nSecond passage.\n\n# The story\n..."
};
</script>
```

## Credits

Built for a TEDx speaker who wanted to drill her talk out of order, with errorless-learning habits: retrieval first, the correct version shown only when needed, and no marks on what went wrong.
