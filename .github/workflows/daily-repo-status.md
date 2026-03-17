---
on:
  schedule:
    - cron: '0 9 * * *'
  workflow_dispatch:
permissions:
  issues: write
engine: copilot
tools:
  github:
    toolsets: [issues, pulls, releases, code]
safe-outputs:
  - type: issue
---

# Daily Repository Status Report

Gather the recent activity from this repository for the last 24 hours, including:

- New and closed issues
- Opened, merged, and closed pull requests
- New releases or tags
- Notable code changes and commits

Then create a new GitHub issue titled "Daily Status Report - {today's date}" with the following sections:

1. **Summary** - A brief overview of the day's activity
2. **Issues** - New issues opened, issues closed, and any trending discussions
3. **Pull Requests** - PRs opened, merged, or closed with short descriptions
4. **Releases** - Any new releases or tags
5. **Highlights** - Notable contributions or milestones

Keep the tone concise and informative. If there was no activity, note that the repository was quiet.
