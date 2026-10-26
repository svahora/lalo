# lalo

A proactive assistant that lives in the Mac menu bar. Tell it anything, and it turns it into a task, breaks the task into steps, and does the steps it can.

Each step is tagged:

- **AI**: lalo does it on its own.
- **AI helps**: lalo drafts, researches, or prepares it, and you finish it.
- **You**: a clear next action for you.

Anything that goes out (sending a message, paying) always waits for you.

## What's here

`prototype/index.html` is a clickable prototype in one file. Open it in a browser. It uses example data only, and nothing is connected or sent.

It covers:

- Quick capture from the menu bar (click the spark or press ⌥ Space)
- A board with three columns: Working, Needs you, Done
- Reply drafts, each with its own chat for changes
- A personal errand (buying a stove) with questions, discounts, and a shortlist
- 1:1 prep with context from other teams and a coaching tip
- A profile of you that you can read and edit
- Meetings: record from the menu bar, live transcript, notes, and action items you send to the board
- Insights: personal ideas to save time, and an admin view of patterns across the organization
- A phone layout with "Hey lalo" on the home screen

## Plan for v1 (personal use)

- SwiftUI menu bar app, built with Swift Package Manager
- Local SQLite store
- Each task runs `claude -p` in the background, using your Claude login and connectors (Slack, Linear, Notion, Granola, Google Drive)
- Sending and buying tools are blocked. Drafts stay in lalo until you approve them
- Reply radar: finds Slack messages that need your reply and drafts answers in your voice
- Phone capture: messages to yourself in Slack that start with `+` become tasks
