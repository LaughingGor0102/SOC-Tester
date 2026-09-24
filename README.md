# SOC Shift 🛡️

**Can you defend the network?** SOC Shift is a free, interactive game that puts you in the seat of a security analyst. Alerts arrive one at a time. Some are real attacks, some are harmless. Decide what to do before the clock runs out.

**[▶ Play the live demo](https://github.com/LaughingGor0102/SOC-Tester/)**

No installation, no account, no experience needed. Works on phone and computer.

## Run it locally

Download `index.html` and open it in any browser.

## How to play

1. Open the link and click **Start my shift**.
2. Read the alert: a plain-English story plus the raw log.
3. Choose an action within **25 seconds**:
   - ✅ **Safe**: normal activity, dismiss it
   - 🔍 **Suspicious**: not sure, investigate further
   - 🚨 **Attack**: real threat, block and escalate
4. Read the explanation after each answer, then continue.
5. After 8 alerts, see your score, rank, accuracy and timings, and save your result to the leaderboard.

## Scoring

| Result | Points |
|---|---|
| Correct answer | +100, plus up to +50 speed bonus |
| Win streak | +10 per extra correct answer in a row (max +40) |
| One step away from the best answer | +30 |
| Wrong answer | -50 |
| Time runs out | -25 |
| Using a hint | -20 |

### Ranks

Curious Newcomer → Junior Analyst → SOC Analyst → Senior Analyst → Threat Hunter

## What you learn

Each alert is based on a real attack technique or a common false alarm, and is mapped to the [MITRE ATT&CK](https://attack.mitre.org/) framework where relevant:

- Brute force and password spraying
- Impossible travel and stolen credentials
- Data exfiltration
- Phishing and lookalike websites
- Malicious document macros
- Persistence through new admin accounts
- Port scans
- Harmless look-alikes (backups, approved scans, normal logins), which teach why alert fatigue matters

## Why I built it

Entry-level security jobs ask for hands-on experience, but most people never get to see real alerts or practise triage decisions. SOC Shift is a safe place to practise, and it lets non-specialists see what defending against attacks feels like.

## Important notes

- **All data is simulated.** IP addresses use reserved example ranges. Nothing touches a real network.
- This is a training and demonstration tool, not a real security monitoring product.
- The leaderboard is stored in your browser (`localStorage`), so it shows scores from your own device only.

## Tech

- Single-file app: plain HTML, CSS and JavaScript, no dependencies or build step
- Responsive, with light and dark mode support
- Hosted on GitHub Pages

## Add your own alerts

Alerts live in the `A` array at the top of the script in `index.html`. Each one has a title, source, story, log, hint, answer (`0` safe, `1` suspicious, `2` attack), technique and explanation.

## Author

**Lavin Wong**, BSc Cyber Security (First Class Honours), Manchester Metropolitan University.

Feedback and suggestions are welcome. Open an issue or get in touch.
