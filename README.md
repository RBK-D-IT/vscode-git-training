# VS Code Git Workflow Training — Instructor Pre-Session Checklist

## Repository

The practice repository is live and public — no attendee access management needed:
**https://github.com/RBK-D-IT/git-vscode-practice**

Anyone can clone it without a GitHub account or PAT. A PAT is only required in
Section 5 when attendees push to their personal forks.

## Before the session

1. Confirm the repo is public:
   `gh repo view RBK-D-IT/git-vscode-practice --json visibility`
   Expected output: `{"visibility":"PUBLIC"}`

2. Add a starter file to the repo so it has content beyond the README.
   Suggested: a `CONTRIBUTING.md` explaining the fork → PR workflow, or a simple
   `data-notes.md` attendees can reference.

3. Share the URL with attendees in advance so they can visit it before the session:
   https://github.com/RBK-D-IT/git-vscode-practice

## Attendee pre-flight (confirm at session start)

- Git for Windows installed (includes Git Bash and Git Credential Manager)
- VS Code installed with the **GitHub Pull Requests** extension
- Each attendee has a GitHub **personal account** (free tier is fine)
- A Personal Access Token with scope `repo` — needed for Section 5 push to fork
- VS Code integrated terminal set to Git Bash:
  File → Preferences → Settings → search "terminal.integrated.defaultProfile.windows" → set to "Git Bash"

## Section 5 — what attendees must personalise before running

Two cells require editing before running (placeholders are clearly marked with ✏️):

| Cell | Placeholder | Replace with |
|------|-------------|--------------|
| Cell 24 (add fork remote) | `<your-username>` | Their GitHub username |
| Cell 26 (create branch) | `<your-firstname>` | Their first name, lowercase |
| Cell 28 (create file) | `<your-firstname>` | Their first name, lowercase |
| Cell 30 (push) | `<your-firstname>` | Their first name, lowercase |

Each attendee ends up with a unique branch (`feature/greeting-alex`) and a unique
file (`hello-alex.md`), so there are no merge conflicts when you merge all PRs.

## After the session (optional)

Merge all attendee Pull Requests from the GitHub web UI to show the collaborative
result — a repo populated with everyone's greeting files. Good closure activity.

## Repository layout after notebook completion

```
~/git-training/
├── git-vscode-practice/       (cloned from RBK-D-IT in Section 3)
│   ├── README.md
│   └── hello-<firstname>.md   (created per attendee in Section 5)
└── my-local-project/          (created locally in Section 4)
    ├── hello_world.py
    └── notes.md
```
