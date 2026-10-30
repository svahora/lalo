# lalo

A proactive work assistant that lives in the Mac menu bar. It reads your work across Slack, your calendar, meeting notes, Notion, Linear, and email. Then it tells you what matters today and gets the work ready before you ask.

Tell it anything, and it turns it into a task with a plan. Each step is tagged:

- **AI**: lalo does it on its own.
- **AI helps**: lalo drafts, researches, or prepares it, and you finish it.
- **You**: a clear next action for you.

Anything that goes out (a message, a comment, a report, a payment) always waits for your approval.

## Try it

Open the prototype at [svahora.github.io/lalo/prototype](https://svahora.github.io/lalo/prototype/), or open `prototype/index.html` in a browser. It is one file and uses example data only. Nothing is connected or sent.

The prototype opens as a **new user**, at the start of setup. To see the app as an **existing user**, use the **Prototype view** switch in the center of the menu bar. On a phone, the switch is at the bottom of Profile.

## What's in the prototype

### Getting started
- **Setup in six steps:** welcome, connect your tools, watch lalo read in, confirm what it learned about you, choose how it checks in, then open Today.
- **Get started checklist** on Today for new users: approve a draft, add a task, and try "Hey lalo".

### Today
- **The top three things** that matter today.
- **Due today:** lalo drafts the work for you. For example, it suggests a comment for a doc and builds an expense report from your receipts.
- **Waiting on your reply:** who asked, where, how long they have waited, and a draft that is ready.
- **Today's meetings:** prep notes for each meeting, a tag when two meetings clash, and a note when no past notes were found.
- **For you** and **Getting to know you:** other items that need you, and things lalo noticed about how you work.
- Each section is one row with a short summary. Click a row to open it in a side panel.

### Menu bar
- A quick recap that changes with the time of day. Step through items with Next.
- Add a task or ask a question. Click the mic, or say "Hey lalo".
- Today's meetings, with a countdown to the next one.

### Tasks
- **Board:** Needs you, Agent working, and Done.
- **New task** from any page (or press N). lalo plans it with you before it starts.
- **Catch up** in the sidebar opens the next item that needs you.
- **Task details** in a side panel: reply drafts in your voice, a code change with screenshots to approve, a personal errand, and 1:1 prep.

### Meetings
- **Coming up:** grouped by day, with time ranges and a countdown to the next meeting.
- **A nudge to record** when a meeting starts.
- **Past meetings:** notes you can edit in markdown, action items, and the transcript.
- **Ask this meeting:** ask a question, and the answer quotes the transcript.

### Signals
- **Weekly pulse:** survey scores with trends, friction themes from Slack, competitor moves linked to themes, and a watchlist of single mentions.
- **Sources:** choose the Slack channels, the competitors and pages to watch, the surveys, and the schedule.

### Also
- Insights with ideas to save time, for you and for the organization.
- A profile of you that you can read and edit.
- Light and dark mode, and a phone layout.

## Plan for v1 (personal use)

- SwiftUI menu bar app, built with Swift Package Manager
- Local SQLite store
- Each task runs `claude -p` in the background, using your Claude login and connectors (Slack, Linear, Notion, Granola, Google Drive)
- Sending and buying tools are blocked. Drafts stay in lalo until you approve them
- Reply radar: finds Slack messages that need your reply and drafts answers in your voice
- Phone capture: messages to yourself in Slack that start with `+` become tasks
