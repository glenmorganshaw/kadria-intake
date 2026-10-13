# Kadria Character Intake: link wrapper

A one-page host for the Character Intake form (an Apps Script web app). The QR code and shared links point **here**, and this page shows
the form in a frame.

Why: on iPhone, a link to `script.google.com` is claimed by the Google Drive app (Universal Link), which cannot open a web app
("unable to open the file"). A link to this page is not claimed by any app, so it opens in the browser, and the form loads inside it.
The form's own server code allows framing (`setXFrameOptionsMode(ALLOWALL)` in `doGet`).

- `index.html` is the whole site. The form address is written in it once; when the Apps Script deployment changes, edit the `src` and the fallback link.
- Nothing is stored here and there are no scripts beyond a 12-second "taking a while" hint.
- Source of truth for the Intake code and notes: the Kadria vault, `_Agent-Only/code/kadria-appscript`.
