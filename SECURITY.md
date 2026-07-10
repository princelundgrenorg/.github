# Security policy

This is the **default security policy** for every repo in the
[princelundgrenorg](https://github.com/princelundgrenorg) organization.
Individual repos may publish their own `SECURITY.md` to override or
extend this.

The apps in this org are macOS native software that typically
requests permissions like Accessibility, Input Monitoring, Login
Items, and (for some apps) IOKit access. A vulnerability in any of
them could be used to read keystrokes, synthesize input, or run
code at login on a user's Mac. Security reports are taken seriously.

## Reporting a vulnerability

**Please do not open a public GitHub Issue for security reports.**
A public report tells potential attackers about a flaw before
users have had a chance to update.

Use one of these private channels instead:

1. **GitHub Security Advisories** (preferred). On the affected repo,
   open the **Security and quality** tab (or the "···" menu if you
   don't see it directly) and click "Report a vulnerability". Only
   the maintainers can see the report, and we can use the same
   thread to coordinate a fix and publish a CVE if appropriate.

2. **Email.** If you'd rather use email, send to the address
   listed on the [maintainer's GitHub profile](https://github.com/princelundgren).
   Please include the affected app's name in the subject line so
   it doesn't get lost.

In your report, please include:

- A clear description of the issue and its impact.
- A minimal reproduction (steps, sample input, screen recording —
  as much as is practical).
- The affected app's version (`App → About <App>`) and macOS
  version you observed it on.
- Any suggested fix or mitigation, if you have one.

## What you can expect

- **Acknowledgement within 72 hours** of receiving the report.
- **An initial assessment within 7 days** — confirmation of
  severity and a tentative timeline for a fix.
- **Coordinated disclosure.** We'll work with you on a public-
  disclosure timeline that gives users time to update. Default is
  90 days from initial report, shortened if a fix ships earlier
  and lengthened if the fix is non-trivial.
- **Public credit** in the fix's release notes if you want it.
  No bug bounty program at this point — these are small
  independent projects.

## Out of scope

Issues that are NOT considered security vulnerabilities for the
purposes of this policy:

- Bugs that require physical access to an already-unlocked Mac.
- Bugs that require malicious software already running on the
  user's Mac with the same permissions as the app.
- Theoretical attacks without a working proof of concept.
- Issues in macOS, Xcode, or third-party dependencies (Sparkle,
  Sentry, etc.) — please report those upstream.

If you're not sure whether something qualifies, err on the side
of reporting privately. We'd rather decline an out-of-scope
report than miss a real one.
