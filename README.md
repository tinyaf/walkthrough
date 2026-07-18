# walkthrough
App for walkthrough with tenants on Move In / Move Out property conditions. To work standalone from Claude ai

PROPERTY WALKTHROUGH APP — STANDALONE VERSION
================================================

This folder contains a complete, self-contained web app:
  - index.html      (the app itself)
  - icon-180.png     (home screen icon)
  - favicon.png       (browser tab icon)

It does NOT need Claude, a chat link, or an internet connection to run once
it's hosted. All your entries and photos are saved on your own device using
your browser's local storage (IndexedDB) — nothing is sent to a server.

WHY IT NEEDS TO BE "HOSTED" AT ALL
-----------------------------------
Since iOS 18.5, Apple blocks JavaScript from running in HTML files opened
directly from the Files app or Safari's local file view. The fix is simply
to put these files on a real (free) web address — after that, everything
runs normally, entirely on your phone.

EASIEST OPTION: GITHUB PAGES (free, permanent, no coding)
-----------------------------------------------------------
1. On your phone or computer, go to github.com and create a free account
   (if you don't have one already).
2. Tap the "+" icon → "New repository." Name it anything (e.g.
   "walkthrough-app"). Set it to Public. Create it.
3. Tap "Add file" → "Upload files." Upload index.html, icon-180.png, and
   favicon.png from this folder.
4. Go to the repo's Settings tab → Pages (left sidebar). Under "Branch,"
   choose "main" and Save.
5. GitHub will give you a URL like:
      https://yourusername.github.io/walkthrough-app/
   That's your permanent link. Open it in Safari.
6. In Safari, tap Share → "Add to Home Screen." Now you have an app icon
   that opens full-screen, with no browser bar, no Claude link needed.

ALTERNATIVE: NETLIFY DROP
---------------------------
Go to app.netlify.com/drop in a browser (may require a free Netlify login)
and drop this whole folder (or a zip of it) onto the page. It will give you
an instant public URL you can open in Safari and add to your Home Screen
the same way.

SHARING WITH OTHER LANDLORDS / STAFF
--------------------------------------
Once hosted, anyone with the link can open it and use it — but note that
IndexedDB storage is PER DEVICE, not shared. If two people open the same
link on two different phones, they each get their own independent data;
one person's entries/photos won't appear on the other's phone. This is
a single-user tool per device, not a shared multi-user database.
