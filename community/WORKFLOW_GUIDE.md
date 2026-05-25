# GitHub Workflow Guide
## For Mark and Lindsay — Getting Started

**Last updated:** May 2026

This is the practical guide for the two of you. Not general GitHub documentation — just what you need to know to use this repository effectively right now.

---

## The Mental Model

Think of GitHub like a shared Google Doc with a superpower: it keeps a permanent record of every version of every file, who changed it, when, and why. You can always go back. You can always see what changed. Nothing is ever lost.

The difference from Google Docs: changes are proposed and reviewed before they're merged in. That's the pull request workflow. It sounds bureaucratic but for a two-person team it's actually just a useful habit — it means nothing changes without at least a moment of intentionality.

---

## The Two Roles

**Mark — Founder, primary maintainer**
- You own the repository
- You review and merge changes
- You write the journal entries
- You make the calls on governance documents

**Lindsay — Media Director, primary contributor to `/design`**
- You own the Prompt Library and Design Decisions documents
- You propose changes via pull request
- You don't need to touch governance or journal files unless you want to
- Your workflow is entirely through the GitHub web interface — no terminal needed

---

## Mark's Workflow

### Setting up the repository

1. Go to github.com and create an account if you don't have one
2. Click the "+" in the top right → "New repository"
3. Name it `csc-foundation`
4. Set it to **Public** (this signals that you build in the open)
5. Do not initialize with a README — you'll upload yours
6. Click "Create repository"
7. Use the "uploading an existing file" link to upload all the files from this session

### Reviewing a pull request from Lindsay

1. You'll get an email notification when Lindsay proposes a change
2. Click through to the PR on GitHub
3. Read the "Files changed" tab — green lines are additions, red are removals
4. Leave a comment if you have questions or want changes
5. Click "Merge pull request" when you're happy with it
6. That's it

### Writing a journal entry

1. Go to the `journal/` folder in the repository
2. Click "Add file" → "Create new file"
3. Name it `YYYY-MM-short-title.md` (e.g., `2026-06-board-search.md`)
4. Paste in the summary from your Claude conversation
5. Click "Commit new file" at the bottom
6. Write one sentence describing what you added
7. Done — no pull request needed for your own journal entries

---

## Lindsay's Workflow

### Your first pull request (do this first)

1. Go to the `csc-foundation` repository on GitHub
2. Navigate to `design/PROMPT_LIBRARY.md`
3. Click the pencil icon (Edit this file)
4. Add the most recent Lovable prompt you used — the one that worked best
5. Scroll to the bottom
6. Under "Propose changes," write one sentence: "Added [description of prompt]"
7. Click "Propose changes"
8. On the next screen, click "Create pull request"
9. Mark will get a notification and merge it

That's the whole workflow. You just did version control.

### Keeping the Prompt Library current

Every time a prompt works well in Lovable or Midjourney:
1. Open `design/PROMPT_LIBRARY.md`
2. Click the pencil to edit
3. Add the prompt with a short description of what it does and why it worked
4. Propose changes → Create pull request

This is your most important contribution to the repository. A well-maintained prompt library is worth more than any other design artifact.

### Updating Design Decisions

When a major design decision is made (new typeface, color change, layout shift):
1. Open `design/DESIGN_DECISIONS.md`
2. Edit the relevant section
3. Add a note at the top of the file: `**Last updated:** [date] — [one sentence about what changed]`
4. Propose changes → pull request

---

## Using Claude with GitHub

The most effective workflow we've found:

**For document updates:**
1. Copy the contents of a file from GitHub (click the file, then the copy button)
2. Paste it into a Claude conversation
3. Say what you want to change or add
4. Claude rewrites the relevant section
5. Copy the result back into GitHub via the edit interface
6. Propose changes

**For building new things:**
1. Work with Claude in a conversation until you have something worth saving
2. Ask Claude to format it as a markdown document
3. Create a new file in the right folder on GitHub
4. Paste it in

**For the Family Feed demo (when you're ready):**
1. Claude will write the React component code in a conversation
2. You create a new repository called `routine-stability-feed-demo`
3. Paste the code in
4. The demo lives at its own URL and can be shared independently

---

## What Lives Where

| Content | Location | Who maintains it |
|---------|----------|-----------------|
| Mission, philosophy | `docs/MISSION.md` | Mark |
| Governance | `docs/GOVERNANCE.md` | Mark |
| Board formation | `docs/BOARD.md` | Mark |
| Design decisions | `design/DESIGN_DECISIONS.md` | Lindsay |
| Prompt library | `design/PROMPT_LIBRARY.md` | Lindsay |
| Journal entries | `journal/` | Mark |
| Contributing guide | `community/CONTRIBUTING.md` | Both |

---

## The One Rule

**Write a sentence explaining every change.** GitHub calls this a "commit message." It doesn't need to be long. "Added board timeline" or "Updated Margaret gradient" is enough. The record of why things changed is as valuable as the changes themselves.

---

*Questions? Stuck? Ask in the Claude Project and we'll work through it.*
