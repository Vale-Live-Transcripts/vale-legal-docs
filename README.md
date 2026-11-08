# Vale! legal documents

The Impressum (legal notice, DDG), Datenschutzerklärung (privacy policy,
DSGVO/GDPR) and Nutzungsbedingungen (terms of use) for Vale!, an app in
development for iPhone, iPad and Mac that shows what is said in the room as
large live text, in German and English. The German terms of use are the
binding version. This repo is the only copy: the website's footer links
here, and the app (once released) and the privacy policy URL in App Store
Connect will point here too.

## Published at

GitHub Pages serves `main` from the repo root:
<https://vale-live-transcripts.github.io/vale-legal-docs/>

| Document | German | English |
|---|---|---|
| Impressum | [impressum.de.html](https://vale-live-transcripts.github.io/vale-legal-docs/impressum.de.html) | [impressum.en.html](https://vale-live-transcripts.github.io/vale-legal-docs/impressum.en.html) |
| Datenschutzerklärung | [datenschutzerklaerung.de.html](https://vale-live-transcripts.github.io/vale-legal-docs/datenschutzerklaerung.de.html) | [datenschutzerklaerung.en.html](https://vale-live-transcripts.github.io/vale-legal-docs/datenschutzerklaerung.en.html) |
| Nutzungsbedingungen | [nutzungsbedingungen.de.html](https://vale-live-transcripts.github.io/vale-legal-docs/nutzungsbedingungen.de.html) | [nutzungsbedingungen.en.html](https://vale-live-transcripts.github.io/vale-legal-docs/nutzungsbedingungen.en.html) |

If a file is renamed or the site moves, change the app's `LegalLinks` (in
the private app repo, once it exists) in the same release, and the footer
links in [vale-webpage](https://github.com/Vale-Live-Transcripts/vale-webpage).

## Editing

- **Keep both languages in sync.** Any sentence changed in one language
  changes in the other in the same commit, and the sections stay in the same
  order.
- Update the "Stand" / "Last updated" date in both files of a document when
  its content changes.
- **The terms of use carry a version number** ("Version 1" next to the date).
  The app will ask every user to agree to the terms before they use it, and
  a `TermsOfUse.version` in the app repo will mirror this number. A change
  that affects users' rights or duties bumps the version in both files and in
  the app in the same release, so the app asks again. Keep the version it
  replaces as an archive copy, `nutzungsbedingungen-v<N>.de.html` and
  `nutzungsbedingungen-v<N>.en.html` (`<N>` is that version's number), so
  what a user agreed to stays readable. Typos and pure clarifications keep
  the version. Until the app's first release the terms may still be revised
  without a new version, as they say themselves.
- The agreement in the app reads "I agree to the Terms of Use" (a
  declaration, as German law requires), never "I have read".
- **Keep the documents true to the app.** The privacy policy names every
  place data leaves the device. Its section "The Vale! App" says what the
  released app does (the microphone, the text kept only in memory, the
  settings on the device, Apple's speech model download, Send Feedback),
  beside this site, the website, the feedback form, Vercel and GitHub. A
  change to the app that adds a place data goes (a new model download, a
  sync, a saved transcript) updates that section in every language, with what
  it is, the provider and its privacy link, the types of data, the data
  subjects, the purpose, retention and the legal basis, and keeps it matched
  to the app's privacy manifest and the App Privacy label in App Store
  Connect.
- Each file is a standalone page: a short shared header (charset, viewport,
  `style.css`, language switch) around the document text. Edit only the text
  between the language switch and `</main>`.
- The privacy policy is adapted from text made with Datenschutz-Generator.de
  (Dr. Thomas Schwenke) and the Impressum follows eRecht24. Keep the generator
  attribution at the end of the privacy policy; the free generator licence
  requires it. For that reason this repo has no open-source licence.
- `.nojekyll` makes Pages serve the files exactly as committed.
- This repo has only `main`, and a push publishes: push only an approved
  change. Commits use the app repo's bracket tags (`[+]`, `[-]`, `[*]`,
  `[#]`), one line, no trailers.
