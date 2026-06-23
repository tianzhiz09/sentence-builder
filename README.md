# Sentence Builder from Texts

An interactive, browser-based grammar app for ESL students learning English syntax through real reading. Students explore the difference between **simple**, **compound**, and **complex** sentences using either a built-in sample text (Donald Batchelder's *"The Green Banana"*) or their own pasted/uploaded text.

The whole app is a single `index.html` file — pure HTML, CSS, and vanilla JavaScript. No login, no server, and no internet connection needed once the page is open.

## Live site

If published with GitHub Pages, the app is available at:

```
https://YOUR-USERNAME.github.io/REPO-NAME/
```

(Replace `YOUR-USERNAME` and `REPO-NAME` with your own once Pages is enabled.)

## What students can do

**Choose Your Text**
- Use the built-in sample text, **or**
- Paste their own short text, **or**
- Upload a plain `.txt` file.

The app then splits the text into sentences and builds four games from it.

**The four games**
1. **Find the Clauses** – identify and label independent and dependent clauses, then decide the sentence type. Two modes: the app picks sentences, or the student chooses one.
2. **Sort the Sentences** – drag (or tap) sentence cards into Simple, Compound, or Complex columns.
3. **Choose the Connector** – combine two ideas with the best connector (*and, but, so, because, although, when…*) and see how it changes the sentence type.
4. **Change the Sentence** – transform a sentence into a new type (simple → compound, simple → complex, and more).

All movable items support both **drag-and-drop** and **click-to-move**, so the app works well on tablets and touch screens.

## A note on accuracy

This is a **practice tool**, not a grammar grader. For the built-in text it uses teacher-created answer keys; for student texts it uses simple rule-based guesses. Some sentence types may need teacher review — the app says so to students.

## For teachers: editing the activities

All content lives in clearly labeled JavaScript arrays at the top of the `<script>` section in `index.html`, under the comment:

```js
// Teachers can edit the sample text, answer keys, connector questions, and transformation tasks below.
```

You can edit:
- `sampleTexts` – the built-in reading passage
- `greenBananaClauseExamples` – clause analyses for *Find the Clauses*
- `greenBananaSentenceKey` – answer key for *Sort the Sentences*
- `connectorQuestions` – items for *Choose the Connector*
- `transformationTasks` – tasks for *Change the Sentence*

To add a new activity, copy one `{ ... }` object in the relevant array, paste it below, and change the text. Save the file and re-upload it to update the live site.

## Publishing with GitHub Pages

1. Create a new **public** repository on GitHub.
2. Upload `index.html` (and this `README.md`).
3. Go to **Settings → Pages**, set the source to **Deploy from a branch**, choose `main` / `/ (root)`, and **Save**.
4. After a minute or two, your link appears on that same page. Share it with your students.

> The home page file **must** be named `index.html` for GitHub Pages to load it automatically.

## Accessibility

- Large, readable text and clearly labeled buttons.
- Color is never the only signal — every color-coded item also has a text label.
- Works with click interaction alone (drag-and-drop is optional).
- Responsive layout for laptop and tablet screens.

## License

Free to use and adapt for educational purposes.
