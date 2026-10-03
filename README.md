> [!IMPORTANT]
> **Supermail is now MemDesk, and has moved to
> [github.com/michaelbeijer/MemDesk](https://github.com/michaelbeijer/MemDesk).**
> This repository is no longer updated: get the latest version, the guides and
> the phone app's Code.gs there.

<p align="center">
  <img src="icons/icon.svg" width="112" height="112" alt="">
</p>

<h1 align="center">MemDesk</h1>

<p align="center">
  <b>A Kanban board, a notebook and your week, inside Gmail.</b><br>
  Every card is an email. Every note is a message in your own mailbox.<br>
  Your calendar with your tasks in it. No server, no database, nothing to sign up for.
</p>

<p align="center">
  <img alt="Version 0.18.0" src="https://img.shields.io/badge/version-0.18.0-6D28D9">
  <img alt="Chrome, Manifest V3" src="https://img.shields.io/badge/Chrome-Manifest%20V3-7C3AED">
  <img alt="Android: Gmail panel and home-screen app" src="https://img.shields.io/badge/Android-panel%20%2B%20app-8B5CF6">
  <img alt="No server" src="https://img.shields.io/badge/server-none-9F67FA">
  <a href="LICENSE"><img alt="MIT licence" src="https://img.shields.io/badge/licence-MIT-A78BFA"></a>
</p>

<p align="center">
  <a href="#what-it-does">What it does</a> ·
  <a href="SETUP.md">Set it up</a> ·
  <a href="#usage">How to use it</a> ·
  <a href="#privacy">Privacy</a>
</p>

<p align="center">
  <img src="images/hero.jpg" width="100%" alt="Three Chrome windows, one for each tab - the board, the notes and the calendar - with the phone app's week in front of them">
</p>

## What it does

### 📋 A board made of your email

Columns are Gmail labels and cards are threads. Drag a card and its label
moves with it; drop it on **Done** and it leaves the Inbox. Give a card your
own title, a note and a colour without touching the email itself. Light or
dark, as Chrome is.

<img src="images/board.jpg" width="100%" alt="The board in Gmail: To do, Doing, Waiting and Done, half in light mode and half in dark">

### ✉️ Right where you read

While you read an email, one button at the bottom of Gmail says where it is on
the board, and files it in a column without opening the board.

<img src="images/gmail.jpg" width="100%" alt="An email open in Gmail, with the On board: Doing menu open below it">

### 📝 Notes that live in Gmail

Headings, bold and italics, lists, checklists you tick, links. Notes save as
you type, and a paste from Word, Google Docs, a web page or Markdown arrives
formatted. Folders nest as deep as you like, and fold away when the tree gets
long.

<img src="images/notes.jpg" width="100%" alt="The notes: nested folders on the left, the list in the middle, a checklist note open on the right">

### ✏️ A Scratchpad, always open

Open the notes and you are already in it, cursor blinking: one note for
whatever needs writing down right now, and the same one on every computer and
phone, so a line jotted on the train is waiting at your desk. On the phone it
fills the screen under the search box; in Chrome it is open whenever no other
note is, and pinned at the top of the list.

<img src="images/scratchpad.jpg" width="100%" alt="The Scratchpad open in Chrome beside the notes list, and on a phone, where the app opens on it">

### 🔎 Search that shows you where

The words you searched for are marked in the list and in the open note, with
a find bar to step from one to the next.

<img src="images/search.jpg" width="100%" alt="A search for termbase, marked in the results and in the open note">

### 📅 Your week, tasks and all

A third tab: your Google Calendar with Google Tasks woven into it. The week
as seven columns, the month, or the next four weeks as one list. A task with
a date sits in its day, ready to tick; the ones without a date, and any that
are overdue, wait at the side; a task made from an email opens the email.
Every calendar and task list shows or hides with one click. On the phone it is
the week as two columns of days, with the month as the eighth, swiped to the
next week. It only reads, for now: ticking tasks off, due dates on cards and
adding events are next.

<img src="images/calendar.jpg" width="100%" alt="The calendar in Gmail: a week of events and tasks beside a small month, the calendars and the tasks with no date; on a phone, the same week as two columns of days">

### 📱 And on your phone

A home-screen app with the board, the notes and the calendar: the board one
column to a screen, swiped sideways; the notes opening straight onto your
Scratchpad, ready to type, with the same editor, folders and search as in
Chrome; your week as two columns of days. And a panel in the Gmail app files
the open email on the board, ticks your checklists and adds to a note.

<img src="images/phone.jpg" width="100%" alt="Three phones: the board, the Scratchpad, and the week as two columns of days">

### 🔒 Yours alone

There is no MemDesk server and no account to make. The board and the notes
are views of your own mailbox, and the calendar of your own Google Calendar
and Tasks, through Google's API, from your own browser. MemDesk never sends
mail, never deletes anything for good, and only reads your calendar. See
[Privacy](#privacy).

## How it works

A Kanban board and a notes system inside Gmail, for one person, backed
entirely by Gmail itself.

Every card is a Gmail thread and every column is a Gmail label (`_Board/To do`,
`_Board/Doing`, `_Board/Waiting` and `_Board/Done` to start with). Moving a card
moves the label. Every note is a message in your own mailbox, never sent, filed
under `_Notes`. There is no separate database and no server: the board and the
notes are views of your mailbox. Because they are ordinary labels and messages,
they show up in the Gmail app on your phone too, so you can file a thread from
the train and see it on the board later, or look up a note. The leading
underscore sorts both labels to the top of Gmail's label list. The board and the
notes editor themselves only exist in desktop Chrome; on a phone, the **phone
panel** (a small Gmail add-on you install for yourself, see below) puts the
open email in a column, ticks checklist items, adds lines to a note, files it
in a folder and starts new notes from inside the Gmail app, and the **phone
app** puts the notes themselves, with the full editor, on your home screen.

The **Calendar** tab reads Google Calendar and Google Tasks with a sign-in of
its own (read-only), asked for the first time you open it, so the board and
the notes never depend on it.

Version 0.18.0 (called Supermail until 0.17.1). Plain JavaScript, Manifest V3, no build step and no runtime
dependencies for the extension; the phone panel is one generated Apps Script
file.

## Getting started

**Sent a link to MemDesk?** Then **[INSTALL.md](INSTALL.md)** is all you
need: add it to Chrome, click **Connect Gmail**, done - about two minutes.

**Setting up your own copy** from this repository? **[SETUP.md](SETUP.md)**
walks through it step by step:

1. **The extension** (Chrome on a computer): download, load it in
   `chrome://extensions`, and connect it to Gmail through a free Google Cloud
   project of your own. About 15 minutes, once.
2. **The phone panel** (the Gmail app): paste two files into a new Apps Script
   project. About 5 minutes.
3. **The phone app** (a home-screen icon): one more click in that same
   project. About 3 minutes.

It works with Google Workspace and with @gmail.com accounts.

The manifest carries a public `key`, so the extension ID - and with it the
redirect URI that every user's OAuth client needs - is the same on every
install:

| | |
|---|---|
| Extension ID | `lfeogecmdohgofbifobhkolapmjikdih` |
| Redirect URI | `https://lfeogecmdohgofbifobhkolapmjikdih.chromiumapp.org/` |

The matching private key is not in the repository and is not needed to load the
extension. It only matters if you ever pack a `.crx`.

## Usage

- **Open the board** with the **Board** button at the bottom left of Gmail, the
  toolbar icon, or **Alt+Shift+K**. Change the shortcut at
  `chrome://extensions/shortcuts`. Press **Esc** to close it.
- The first time you open it, the board creates any column labels that are
  missing, plus their parent (`_Board`) so Gmail nests them in the sidebar.
- Columns remember their label's id as well as its name, so renaming a label in
  Gmail itself (say `Board` to `_Board`, which renames every column label under
  it) is followed rather than answered with a fresh, empty label. New columns
  go under whatever parent the existing ones share.
- **Drag** a card to another column, or within a column to reorder it. A
  placeholder shows where it will land.
- Each card's **⋯** menu offers the same actions without a mouse: Open in Gmail,
  Move to another column, and Remove from board.
- **Edit card…** on the same menu gives a card your own title, a note and a
  colour. The title replaces the subject on the board, the note replaces the
  email preview, and the colour shows as a stripe down the card's left edge.
  None of it touches the email: the subject, the labels and what your
  correspondents see stay exactly as they were. Hover over a renamed card to see
  the email's real subject. "Use the email subject" in the editor, an empty note
  and "No colour" put the card back as it was. Enter saves from the title field,
  Ctrl+Enter from the note, and Esc cancels.
- **Click** a card to open the thread in Gmail. Ctrl-click or middle-click opens
  it in a new tab.
- The **+** on a column opens a search box that takes Gmail search syntax
  (`from:anna is:unread`). Leave it empty to list your Inbox. Click a result to
  add it to that column.
- **Done** archives on drop: moving a thread there also takes it out of the
  Inbox. You can switch this on or off for any column.
- The **columns button** in the header adds, renames, reorders and removes
  columns. Renaming a label there renames the Gmail label itself, so the mail
  filed under it stays put. Removing a column only takes it off the board. The
  Gmail label and its mail are left untouched.
- While you are reading a thread, a second button appears next to **Board**:
  **Add to board ▾**, or **On board: Doing ▾** if the thread is already on the
  board. Its menu files the thread without opening the board.
- Cards show the subject, the latest sender ("me" if it was you), how long ago
  the latest message arrived, two lines of the snippet, a message count, a star
  for starred threads, and bold text with a dot for unread ones.
- The board refreshes when you open it if what it shows is more than a minute
  old, and whenever you press the refresh button. Each column loads up to 100
  threads and says so when there are more.
- The setup page can move the buttons to the bottom right or hide them.

Card order within each column is stored in this browser (`storage.local`). The
column layout and your card edits are stored in `storage.sync`, so they follow
your Chrome profile to other computers. All of it is kept per Gmail account.

### Notes

- **Open the notes** with the **Notes** tab next to **Board** at the top of the
  board, or the **Notes** button beside **Board** at the bottom left of Gmail.
  The board reopens on whichever tab you used last.
- **Folders** are in the column on the left: **All notes**, then your folders
  as a tree, each with how many notes it holds. Choose one to see only its
  notes (and to search only inside it). The **+** at the top makes a folder;
  a folder's **⋯** menu renames it (its subfolders come along), makes a
  subfolder, or deletes it - only once it is empty. Move a note by dragging it
  onto a folder (onto **All notes** to take it out of its folder), or with the
  folder button above the note. A new note starts in the folder you are
  looking at. A folder with subfolders has a small arrow beside it that folds
  them away (or the left and right arrow keys, on a folder): handy once the
  tree grows long. Which ones are folded is remembered on that computer. Each
  folder is a Gmail label under `_Notes` - `_Notes/Work`,
  `_Notes/Work/Clients` - so the same tree shows in Gmail's label list on the
  phone.
- The list in the middle shows your notes, newest first, with their first lines.
- The **Scratchpad** is pinned at the top of it, and open on the right
  whenever no other note is: the notes open on it, with the cursor in it, so
  you can start typing at once. It is one note, saved like any other (as
  "Scratchpad" under `_Notes`), and the same one on every computer and phone,
  so a line typed on the phone is waiting in Chrome. It has no folder and
  cannot be renamed or deleted; clear it by deleting its text.
- **Search** shows where the words are. While a search is on, each result shows
  short excerpts around its matches with the words highlighted, and how many
  matches it has; words in titles are highlighted too. Case and accents do not
  matter ("cafe" finds "Café"), a word matches at the start of a word ("gloss"
  finds "glossary"), and "a phrase in quotes" matches as a phrase. Gmail still
  does the finding - operators like `from:` or `before:` work, they are just
  not highlighted. Open a result and every match in the note is highlighted,
  without touching its text: a bar above the title says "2 of 5", and its
  arrows, F3 and Shift+F3 step through them. The ✕ on that bar clears the
  search.
  The **search box** above it runs Gmail's own search inside your notes, so it
  finds words anywhere in a note and takes Gmail syntax (`before:2026/09/01`).
  **New** starts a note.
- The open note is on the right: a title and the text. It **saves itself** a
  couple of seconds after you stop typing, and again when you switch notes or
  tabs or close the board; **Ctrl+S** saves at once. The line above the title
  says "Unsaved changes", "Saving…" or "Saved". Closing the Gmail tab with an
  unsaved change asks before leaving. Enter in the title moves to the text.
- A note with no title is filed under its first line.
- **Delete** moves the note to Gmail's Trash, with an **Undo**. **Open in Gmail**
  shows the note as Gmail stores it.
- **Formatting.** The toolbar above the text has a text style menu (normal text
  and three heading sizes), bold, italic, strike-through, bulleted, numbered and
  check lists, less and more indent (three levels deep), links and clear
  formatting. Keyboard: Ctrl+B and Ctrl+I; Ctrl+K for a link; Ctrl+Shift+7, 8
  and 9 for numbered, bulleted and check lists; Tab and Shift+Tab to indent a
  list item; Ctrl+Enter ticks a check box, as does clicking it. Typing `- `,
  `1. `, `[] `, `[x] ` or `#`, `##`, `###` and a space at the start of a line
  turns it into that list or heading. Enter on an empty list item ends the list;
  Backspace at the start of a list item or heading turns it back into text.
  Ctrl-click a link to open it.
- **Pasting keeps the formatting a note can hold.** From Word, Google Docs, a
  web page or an email: headings, bold, italic, strike-through, links, and
  bulleted, numbered and check lists (nested, too) come across; fonts, colours,
  sizes, images and scripts never do. Spreadsheets and tables arrive as one line
  per row with ` | ` between the cells, heading cells in bold. Paragraphs that
  had space between them keep an empty line between them. Text written in
  Markdown - an answer copied from a chat assistant, say - becomes formatting:
  `**bold**`, `*italic*`, `~~struck~~`, `[links](…)`, `#` headings, `- `,
  `1. ` and `- [ ]` lists, and `| tables |`. A list pasted into a list item
  goes in at that item's level, and pasting in the middle of a line carries
  the rest of the line along after it. **Ctrl+Shift+V** pastes the text alone,
  exactly as copied. **Ctrl+Z** straight after a paste takes it back (one paste
  at a time). Dropping text onto a note does nothing.

How it works: a note is a message placed straight into your mailbox with
`messages.insert`, labelled `_Notes` (and its folder's label, if it is in one)
and nothing else - not Inbox, not unread. It is addressed to you, with you as
Reply-To, but it is from "Notes" at a reserved address that can never send or
receive mail (`notes@notes.invalid`): Gmail files anything from your own address
under Sent, whatever labels it was given. A note is two renderings of the same
content: an HTML part, which is the record - Gmail shows it, formatting and all,
and the editor reads it back - and a plain-text part with bullets, numbers and
☐ / ☑ for Gmail's previews and plain-text mail clients. The editor reads the HTML
with its own small reader rather than the browser's HTML parser, and keeps only
what the toolbar can make: anything else becomes text. It carries an `X-Gkb-Note` header with the note's own id.
Gmail messages cannot be changed once stored, so saving inserts a new version
and moves the previous one to Trash. That makes Gmail's Trash a 30-day version
history: open an old version there to copy text back. If two versions are ever
both live (a save cut short, or two computers saving at once), the newest wins
and the other is moved to Trash the next time the list loads.

Anything else filed under `_Notes` shows up too - an email you sent yourself
from your phone, say. Its bold, italic, lists and links come across; the rest
reads as text. It is marked "From an email".
Editing it saves a new note in its place and takes the email off the list
(it keeps the email, just without the `_Notes` label); Delete does the same.

Like the columns, the notes label is followed by id, so you can rename `_Notes`
in Gmail and the notes follow.

### Calendar

- **Open it** with the **Calendar** tab next to **Notes**, or the **Calendar**
  button at the bottom left of Gmail.
- **The first time**, it asks to connect: **Connect Google Calendar**, then
  allow it on Google's page. It asks for read-only access to Google Calendar
  and Google Tasks, and for your address, to check that the calendar is the
  one of the account open in the tab. This is a sign-in of its own: the board
  and the notes never needed it, and keep working whatever you answer.
- **Week, Month, Agenda** at the top right. The week is seven columns, without
  an hour grid: the times are on the items. The month shows a few things a day
  and "+2 more"; click a day's number to see its week. The agenda is the next
  four weeks as one list, skipping empty days.
- **Today**, **‹** and **›** move about; so do the keys Google Calendar uses:
  **t** for today, **j** or **n** for next, **k** or **p** for previous, and **w**,
  **m** and **a** for the views. The small month on the left goes to the day you
  click.
- **What is on a day**: all-day events first, then the rest by time, then the
  tasks due that day, open ones before ticked ones. An event opens in Google
  Calendar, a task in Google Tasks; a task made from an email in Gmail (with
  an envelope) opens that email.
- **The calendars and task lists** on the left show or hide with a click.
  Until you click, they are as Google Calendar has them (a calendar unticked
  there starts hidden here); after that, this computer remembers.
- **Tasks with no date**, and open tasks whose day has gone by, are listed
  under the calendars.
- **On a phone**, or in a narrow window, it is always the week: two columns
  of days, Monday to Thursday and then Friday to Sunday, with the month as the
  eighth; the calendars are a row of chips above, and the tasks with no date
  below. Swipe sideways for the next or previous week. The button beside
  **›** turns the order round: Monday beside Tuesday, then Wednesday beside
  Thursday, and so on; the phone remembers which you chose.
- It only reads, for now. Ticking tasks off, due dates on cards and adding
  events are the next steps.

### Storage

Chrome's sync storage is small: 100 KB in all, and at most 512 entries. Each
edited card takes one entry, so there is room for hundreds of renamed cards,
fewer if every one carries a long note (notes are capped at 500 characters,
titles at 200). Taking a card off the board deletes its edit. Moving it to Done
keeps it. If the storage ever fills, saving an edit says so rather than failing
silently.

## The phone panel

A Gmail add-on for your own account, built with Google Apps Script, that shows
at the bottom of an open email in the Gmail app on your phone (and in the
side panel of Gmail on a computer). It works on the same notes, in the same way,
as the extension.

- **Open a note** in the Gmail app (they are under `_Notes`, at the top of the
  label list), scroll to the bottom and tap the panel's icon. It shows the note
  with a **check box for each checklist item**, a box for **lines to add at the
  end** (as checklist items, bullets or text; text understands the same
  Markdown a paste does), and the note's **folder**. **Save** saves the lot as
  one new version; the old one goes to Trash, as in the extension. Changing only
  the folder just moves the note.
- **Open any other email** and the panel starts with **This email on the
  board**: the column it is in, or "Not on the board". Choose another and it
  moves at once, as with the button next to **Board** in Chrome: into that
  column only (out of any other), and out of the Inbox when the column is
  Done. "Not on the board" takes the column label off and leaves the email
  where it is.
- Below that, the panel lists your newest notes, with a search box (Gmail
  search, as in the extension), a folder filter, and **New note**. Tap a note
  to open it.
- **Search results show where the words are**, as in Chrome: each note with
  up to two short excerpts around its matches and a match count, the words in
  bold orange (cards cannot colour a background). A note opened from the
  results has every match marked and says how many there are, or that the
  words are only in its title. Operators such as `from:` or `before:` narrow
  the search but are not marked. There is no stepping from match to match: a
  card cannot scroll itself.
- **Find in this note**, at the top of every note: type a word and press
  **Find** to mark it everywhere in the note, with a count. **Only lines with
  it** then shows just the lines that have it (a ⋯ marks each stretch left
  out), which is how you get to a match in a long note on a phone; **Whole
  note** brings the rest back and **Clear** removes the marks. Ticks, lines
  to add and a folder chosen before pressing Find are kept, and Save saves
  them as usual. A note opened from search results starts with the search's
  words in the box.
- **New note** takes a title, some lines (as text, a checklist or bullets) and a
  folder. From a folder's list or from a note, it starts in that folder.
- **All notes** and **New note** are also on the panel's own menu (⋮).
- If the note was changed elsewhere since the panel showed it, Save does not
  overwrite it: you get the latest version, with your new lines still in their
  box, and tick again.
- What the panel cannot do: edit or format text that is already in a note (it
  only adds at the end), rename or create folders, or delete notes. Those stay
  in the extension. A note longer than 80 lines shows its first 80; ticks
  further down are left as they were.
- The board's column settings live in Chrome, where the panel cannot see
  them, so it reads the columns from your labels: every label directly under
  `_Board` is a column, To do, Doing, Waiting and Done first in that order,
  any others after them alphabetically, and only Done archives. If you change
  which column archives in the extension, the panel will not know.

**Setting it up** takes about five minutes: a new Apps Script project with
two files pasted in, then **Deploy → Test deployments → Install**. The steps
are in [SETUP.md, part 2](SETUP.md#part-2-the-phone-panel). To update, paste
the new `Code.gs` over the old one at
[script.google.com/home](https://script.google.com/home) and save; the first
line of `Code.gs` says which version it is.

**What it is allowed to do**: read and change your mail's labels and insert
messages (`gmail.modify`, the same as the extension), run as a Gmail add-on and
see which message is open (`gmail.addons.execute`,
`gmail.addons.current.message.metadata`), read your calendars and tasks for
the phone app's calendar (`calendar.readonly`, `tasks.readonly`), and call
Google's APIs (`script.external_request`, only to `gmail.googleapis.com` and
the Calendar and Tasks APIs). It keeps the
extension's rules in its own code: it inserts only notes, moves to Trash only
messages it has itself checked are notes, never adds Trash, Spam or Inbox to
anything, and never sends. It runs in Google's Apps Script under your account;
nothing goes anywhere else. To remove it: **Deploy > Test deployments >
Uninstall**, and delete the project.

**How it is built**: `addon/Code.gs` is generated by `node tools/build-addon.mjs`
from the shared note code in `src/lib/` (the same files the extension loads)
and the panel's own files in `addon/src/`, with small stand-ins for the browser
APIs Apps Script lacks (`addon/src/shims.js`). `npm test` fails if it is out of
date, and runs the whole panel against the preview's fake Gmail in a stand-in
for Apps Script (`tests/addon.test.js`).

## The phone app

The board and the notes on your phone's home screen: the extension's own
board and Notes view, served full-screen by the same Apps Script project as
the phone panel, and added to the home screen from Chrome. The same
**Board** and **Notes** tabs, columns and cards, notes, folders, search with
the words marked, formatting editor, checklists, find and autosave as in
Chrome, laid out for a phone. (Opened on a computer, it is the board and
notes as in Gmail, in a tab of their own.)

- **The board**, one column to a screen: swipe sideways for the next. A
  card's **⋯** opens it in Gmail, moves it to another column, edits its
  title, note and colour, or takes it off the board; the **+** on a column
  finds an email and adds it; the settings button changes the columns.
  The first time, the columns are your `_Board` labels as Gmail has them;
  after that the app keeps its own column layout and card edits, the same
  on every phone and computer you open it on (but separate from the
  extension's, which Chrome keeps).
- **The notes open on the Scratchpad.** The search box and **New** at the top, and
  the Scratchpad below them, filling the screen: tap it and type.
- **One thing at a time.** Above the search box, one button says which folder
  you are in ("All notes"); tap it and the folder tree opens, nested as on a
  computer, with its counts and each folder's ⋯ menu (rename, new subfolder,
  delete). Pick a folder - **All notes** too - and its list takes the
  Scratchpad's place; so does a search. Tap a note and it opens full-screen.
  Tap the arrow beside a folder to fold its subfolders away, or open them
  again; the phone remembers which are folded.
- **Back** steps back: Android's back gesture (or the arrow at the top left of
  a note) goes from a note to the list it was opened from, and from the list
  to the Scratchpad. The pinned Scratchpad at the top of the list goes there
  too.
- **Saving.** As in Chrome, a moment after you stop typing - and at once when
  you go back to the list or switch to another app, since a phone does not
  close pages.
- **Search** marks the words in the results and in the open note, with the
  arrows to step from one match to the next.
- **The calendar**, the week as two columns of days with the month as the
  eighth: swipe sideways for the next week, tap a chip to show or hide a
  calendar or task list, and the button beside **›** to have the days run
  across rather than down (the phone remembers both). It reads Calendar and
  Tasks with the script's own access, so there is nothing to connect; the
  first time, it may ask you to **Allow** it.

**Setting it up** is one more step in the phone panel's project: **Deploy →
Test deployments → Web app**, open its address in Chrome on the phone, and
**Add to Home screen**. See [SETUP.md, part 3](SETUP.md#part-3-the-phone-app).
The address ends in `/dev`: it always runs the code last saved, and only you
can open it.

**How it works**: `doGet` in `Code.gs` serves the page, which is
`addon/app/index.html` with the extension's own files packed into it
(`src/content/board.js`, `store.js`, `notes.js`, `note-editor.js`,
`calendar.js`, `ui.js`, `styles.js` and the shared code). They go in as base64 inside one small loader script, which runs
them in order and names any that fails: Apps Script takes a page's inline
scripts out and runs them itself, and an app made of many plain scripts did
not survive that (it came up blank). With them come `addon/app/remote.js`, which gives the notes a store, and
the board its Gmail and its settings, that ask the script through
`google.script.run` instead of the extension's background worker (a board's
worth of cards in one round trip); `addon/app/remote-board.js`, the first
column layout from the labels; and `addon/app/shell.js`, which hands the
page to the board (`ns.boardFrame`) and adds the phone layout and the back
gesture.
On the script's side, `addon/src/app-server.js` keeps the worker's rules: it
inserts only notes, moves to Trash or back only messages it has itself
checked are notes, takes an email kept as a note off the list without
touching it otherwise, and deletes a folder only when Gmail says it is empty;
for the board it reads labels and threads, makes and renames labels, and
changes the labels on a conversation - never Trash, Spam or the Inbox, never
anything sent or deleted; for the calendar it makes the same four reads as
the extension (the calendar list, a calendar's events, the task lists, a
list's tasks) and nothing else. The app's column layout and card edits are
kept in the script's user properties. It runs as you, under the phone panel's
permissions, which since 0.17.0 include read-only access to Calendar and
Tasks. Google does not ask for new permissions by itself once a script has
been allowed some, so if the calendar has not been allowed yet, it says so
with an **Allow** button, which opens Google's page for the script (the
function `allowCalendar`, run once in the script editor, does the same).

## Privacy

The privacy policy is [PRIVACY.md](PRIVACY.md). In detail:

- **There is no server.** The extension talks only to Google: to
  `gmail.googleapis.com`, and, for the calendar, to the Calendar and Tasks
  APIs (`www.googleapis.com/calendar`, `tasks.googleapis.com`) and Google's
  userinfo endpoint - from your browser. The phone panel runs in Google's Apps
  Script, under your own account, and talks only to the same APIs (see
  [The phone panel](#the-phone-panel) for what it may do).
- **The access token lives only in this browser's session storage**
  (`chrome.storage.session`). It is held in memory, is not readable by the Gmail
  page or by the content scripts, and is gone when Chrome closes. The implicit
  grant issues no refresh token, so nothing long-lived exists anywhere. Tokens
  last an hour and are renewed silently while you are signed in to Google.
- **What the scope allows.** `gmail.modify` is broad. It permits reading mail
  (including message bodies), changing labels, archiving, moving to Trash, and
  technically sending mail. It does **not** permit permanent deletion; that
  needs the full `https://mail.google.com/` scope.
- **What this code does.** For the board, it reads thread metadata (subject,
  sender, date, label ids and Gmail's snippet), creates and renames labels, and
  adds or removes labels on threads, including `INBOX` when archiving. For the
  notes, it reads the messages under `_Notes` and its folders (bodies
  included), inserts new notes, moves notes between folders, moves its own old
  versions and deleted notes to Trash, and creates, renames and deletes empty
  folders under `_Notes`. It **never
  sends and never permanently deletes**, never touches Spam, and moves nothing
  to Trash but its own notes. The background worker enforces this with an
  allow-list: any other Gmail API call, any `DELETE`, any attempt to add `TRASH`
  or `SPAM` as a label, and any insert that is not a note (a message carrying
  the `X-Gkb-Note` header, filed under user labels only - never Inbox, Sent,
  Drafts, Spam, Trash or unread) is refused before a token is even fetched.
  Before trashing a message, the worker reads that message's headers itself and
  refuses unless it is a note. The only label it will delete is an empty notes
  folder: before a `DELETE`, it reads the label, the full label list, and
  whether any message is still filed under it, and refuses anything that is not
  a folder under the notes label with no notes and no subfolders.
- **One scope, and only that.** The extension's token request asks for
  `gmail.modify` alone, with `include_granted_scopes=false`. Google treats
  every client in a Cloud project as one app, so incremental auth would fold
  any other Gmail grant in the same project (a `gmail.metadata` one, say) into
  this token - and Gmail then applies metadata-scope rules to the whole token,
  and search (`q=`) stops working.
- Every token is checked against Gmail's own profile before use. If Google
  signs in a different account from the one in the Gmail tab, the token is
  discarded and the board says so, rather than acting on the wrong mailbox.
- **The calendar has a token of its own**, asked for separately and only when
  the Calendar tab is opened: `calendar.readonly`, `tasks.readonly` and
  `email` (to check, through Google's userinfo endpoint, that it is the account
  in the tab - the calendar's token cannot read Gmail's profile). Read-only
  scopes, so it could not change a calendar or a task if it tried, and the
  worker lets through only four kinds of `GET`: the calendar list, a calendar's
  events, the task lists, and a list's tasks. It lives in session storage like
  Gmail's, and the two never mix (`include_granted_scopes=false` on both).
  Events and tasks are shown, never stored.

## Known fragile points

These depend on Gmail's page rather than on a documented interface. All of them
live in `src/content/gmail-hooks.js`, and each fails quietly.

- **Account detection** reads the address out of `document.title`
  ("Inbox (3) - you@example.com - Gmail"), falling back to the aria-label of the
  `Google Account` avatar link. If Gmail changes both, the board says it cannot
  tell which account the tab belongs to.
- **The open thread** is read from the `data-legacy-thread-id` attribute on the
  conversation's subject heading, polled once a second while the tab is visible.
  If Gmail drops the attribute, the "Add to board" button simply stops
  appearing. Everything else keeps working.
- **Opening a thread** sets `location.hash` to `#all/<threadId>`, using the
  legacy hex id the API returns. Gmail currently accepts these and redirects to
  its newer ids.
- **Gmail's keyboard shortcuts** are kept out of the board's text boxes by
  stopping key events at the shadow host. If Gmail ever listens for keys in the
  capture phase, typing in the search box could trigger them.
- The **implicit grant** (`response_type=token`) still works for Web
  application clients, but Google discourages it. If it is ever retired, the
  fix is authorisation code with PKCE in the same `launchWebAuthFlow` call.

None of these, nor real OAuth, can be exercised outside real Gmail. The tests
below cover everything else.

## Renaming

The display name appears in exactly these places:

1. `manifest.json`: `"name"`
2. `manifest.json`: `"action"."default_title"`
3. `src/shared/ns.js`: `APP_NAME`
4. `README.md`: the title
5. `addon/appsscript.json`: `"addOns"."common"."name"`, the phone panel's name
   (its cards take theirs from `APP_NAME`; rebuild `addon/Code.gs` after a rename)
6. The setup page title. It is set from `APP_NAME` at runtime, so no edit is needed.
7. The icon's letters: `RUNS` in `tools/icon-svg.py`; then run it and
   `tools/make-icons.mjs` again, and copy the new path into `LOGO` in
   `src/content/ui.js` (a test says if they differ).

The guides (`INSTALL.md`, `SETUP.md`, `PUBLISHING.md`, `PRIVACY.md`) and
`store/listing.md` use the name in their text, and link to the repository by
its address. The pictures take the name from `APP_NAME`: run
`tools/readme-shots.mjs` again.

Nothing internal carries the name: not the `gkb` namespace, the storage keys
(`clientId`, `columns:<email>`, `order:<email>`), the CSS classes or the element
ids. A rename therefore leaves stored data, the extension ID (derived from the
`key`) and the redirect URI unchanged. `tests/static.test.js` fails if the name
turns up anywhere else. The app name on the Cloud consent screen is set
separately in the Cloud console. One exception, from before the last rename:
the phone app keeps its settings in the browser under `supermail.`, its name
until 0.17.1, and keeps that prefix so they survive.

## Running the tests

Unit tests (Node 18 or later, no installs):

```bash
npm test                      # same as: node --test tests/*.test.js
```

These cover auth URL building and redirect parsing, the proxy's allow-list
(Gmail's and the calendar's), the calendar's dates, weeks and views and how
events and tasks become day items (in a time zone with summer time), order
merging, the label arithmetic for moves, entity decoding, address parsing,
account-from-title detection, relative dates, and static checks on the source:
no HTML-string sinks, the name only in the rename spots, and the preview's
script list matching the manifest. Node 22's runner does not accept a bare
directory (`node --test tests/`), so the glob form is used. Node expands it
itself, so it works on Windows too.

Browser checks use `playwright-core`, which is deliberately not a dependency.
Either install it without saving it (`node_modules/` is gitignored), or point
`PLAYWRIGHT_CORE` at an existing copy:

```bash
npm i --no-save playwright-core
npm run test:preview          # (a) content scripts against a fake Gmail
npm run test:extension        # (b) the real unpacked extension
npm run test:app              # (c) the phone app at a phone's size
```

- `CHROMIUM_PATH` chooses the browser. It must be full Chromium, because
  `chrome-headless-shell` cannot load extensions. Otherwise
  `/opt/pw-browsers/chromium-*` is used if present, and then Playwright's own
  download.
- `SCREENS_DIR` is where screenshots go. The default is a folder in the system
  temp directory.
- (a) loads `dev/preview.html` under Trusted Types and drives it: drag between
  and within columns, the ⋯ menu, search-add, column settings, Esc, the dock
  button, dark mode, the connect and setup states, a failing move, and label
  creation. It checks the fake mailbox's labels after each step. And the
  calendar, against a fake Calendar and Tasks: the week, month and agenda,
  the keys, showing and hiding sources, connecting it, Tasks not allowed, and
  the narrow week.
- (b) starts Chromium with `--load-extension`. It tries new headless first and
  falls back to `xvfb-run` if the service worker does not appear. It checks the
  worker, the extension ID, the setup page, the allow-lists, and that the content
  scripts inject into a stand-in `mail.google.com` page and reach the worker.
- (c) opens the phone app's page at a phone's size, with touch, its
  `google.script.run` wired to the real `Code.gs` running in the Apps Script
  stand-in against the fake Gmail: the list and folder chips, opening a note,
  typing and formatting with autosave, ticking a box, the back gesture,
  search, a new note, saving on switching away, the board, the calendar's
  phone week with its chips and swipes, and dark mode.

### Dev preview

Open `dev/preview.html` straight from disk in Chrome. It runs the real content
scripts against a fake `chrome.*` and an in-memory mailbox of about 25 invented
threads. A strip at the top toggles an open thread, sends the shortcut, and
switches between states: `?state=auth_required`, `?state=not_configured`,
`?fail=modify`, `?fresh` (no labels yet), `?page=3` (truncated columns) and
`?latency=600`. `?showcase` swaps the test notes for tidy ones in a deeper
folder tree, for pictures. The calendar has a fake Calendar and Tasks of its
own, a week of invented events and tasks around the current one;
`?calendar=signin` makes it ask to connect first, and `?calendar=notasks`
answers as if Tasks had not been allowed.

### Icons

`icons/icon.svg` is the drawing: "Md" on a violet circle, a member of the
[Supervertaler](https://supervertaler.com) family of icons. `python3
tools/icon-svg.py` draws it (the letters are turned into paths from Liberation
Sans Bold, so it needs `fonttools`), and `node tools/make-icons.mjs` renders it
with Chromium to `icons/icon-{16,32,48,128,192}.png`. The mark inside the app
is the same drawing, kept in step by a test.

### The README's pictures

`node tools/readme-shots.mjs` takes them: the real board and notes in the dev
preview, and the real phone app, against the fake mailbox in its tidy
`?showcase` mode, framed in a browser window and phones, into `images/`.

## Layout

```
manifest.json
src/shared/ns.js           namespace, APP_NAME, storage keys
src/lib/                   pure logic, shared by content scripts, worker and tests
  util.js                  entities, addresses, account detection, dates, pool
  auth.js                  auth URL, redirect parsing, API allow-list
  calendar-logic.js        the calendar: dates and weeks, views, events and tasks
                           as day items, what may be asked of Calendar and Tasks
  board-logic.js           columns, order merge, move label diffs, summaries, card edits
  notes-logic.js           building and reading note messages, what may be inserted
  note-format.js           the formatting model: HTML out and back in, plain text,
                           Markdown and pasted HTML in
  search-logic.js          the words in a query, where they occur, excerpts
src/background/sw.js       OAuth (launchWebAuthFlow), the Gmail API proxy, and the
                           calendar's own sign-in and read-only proxy
src/content/               classic scripts, in manifest order
  gmail-hooks.js           every assumption about Gmail's page
  api.js, store.js         messaging and the shared data layer
  notes-store.js           notes: list, read, save (insert + trash), delete
  ui.js, styles.js         DOM builder, icons, menus, toasts, shadow hosts
  board.js, dock.js        the overlay (header, tabs, board) and the corner buttons
  note-editor.js           the formatted editor and its toolbar
  notes.js                 the Notes tab: list, editor, autosave
  calendar-store.js        Calendar and Tasks: sources, and what is on in a range
  calendar.js              the Calendar tab: week, month, agenda, phone week
  main.js                  wiring
src/options/               setup page
dev/                       preview page, fake Gmail, fake Calendar and Tasks
addon/                     the phone panel and phone app (Apps Script)
  appsscript.json          its manifest
  Code.gs                  generated: shared note code + addon/src + the app's page
  src/shims.js             btoa, TextEncoder, URL and friends for Apps Script
  src/panel-logic.js       pure: a note as card items, ticks, appended lines,
                           board columns from labels
  src/gmail.js, store.js   Gmail over UrlFetchApp, and the notes on it
  src/cards.js             the cards and what their buttons do
  src/app-server.js        the phone app's server side: notes, folders, board,
                           calendar reads, the page
  src/triggers.js          the top-level functions Apps Script calls
  app/index.html           the phone app's page, filled in by the build
  app/remote.js            its notes store, over google.script.run
  app/shell.js             its full-screen frame and phone layout
tests/                     unit tests; tests/e2e/ browser checks;
                           helpers/apps-script.js, a stand-in Apps Script
icons/icon.svg             the icon; icon-*.png are rendered from it
images/                    the README's pictures
tools/icon-svg.py          draws icons/icon.svg
tools/make-icons.mjs       renders the icon PNGs
tools/readme-shots.mjs     takes the README's pictures
tools/build-addon.mjs      builds addon/Code.gs
SETUP.md                   step-by-step setup of your own copy
INSTALL.md                 installing from the store and a shared phone app
PUBLISHING.md              for the publisher: the store build, the shared sign-in
PRIVACY.md                 the privacy policy
store/                     the Chrome Web Store listing and its pictures
tools/package-extension.mjs  the store build (dist/, not committed)
LICENSE                    MIT
```

## Roadmap

- **The calendar, step 2.** Tick tasks off from the calendar; give a card a due
  date from its ⋯ menu, which makes a Google Task linked to the email, so it
  shows on its day here and in Google's own apps.
- **The calendar, step 3.** The **+** on a day: "Dentist 14:30" becomes an
  event, "Pay the invoice" a task.
- **A to-do view.** One flat list across all columns, oldest first, for days when
  a board is too much.
- **A "Needs reply" column**, computed rather than labelled: threads whose
  newest message is inbound and not bulk mail, ranked by who is waiting and
  for how long.

## Licence

MIT. See [LICENSE](LICENSE).
