# `.github`

Org-level community health defaults for
[princelundgrenorg](https://github.com/princelundgrenorg). GitHub
automatically uses files in this repo as defaults for every other
repo in the org — see
[Creating a default community health file](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file).

## What's here

| Path | Inherited by every org repo unless that repo has its own |
|------|----------------------------------------------------------|
| [`SECURITY.md`](SECURITY.md) | Security vulnerability reporting policy |
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Code of conduct |
| [`.github/PULL_REQUEST_TEMPLATE.md`](.github/PULL_REQUEST_TEMPLATE.md) | Default PR body template |
| [`.github/ISSUE_TEMPLATE/bug_report.yml`](.github/ISSUE_TEMPLATE/bug_report.yml) | Generic bug report form |
| [`.github/ISSUE_TEMPLATE/feature_request.yml`](.github/ISSUE_TEMPLATE/feature_request.yml) | Generic feature request form |
| [`.github/ISSUE_TEMPLATE/config.yml`](.github/ISSUE_TEMPLATE/config.yml) | Disables blank issues + adds security contact link |
| [`profile/README.md`](profile/README.md) | Org-page README shown at github.com/princelundgrenorg |

## How overrides work

If a repo has its own file at the same path, **that file wins**.
GitHub doesn't merge or splice — it's all-or-nothing per file. So
an app's own repo-specific `bug_report.yml` (with fields specific
to that app) still applies there, but `SECURITY.md` and the PR
template come from here unless a repo overrides them too —
PrinceMouse and PrinceLauncher, for example, each keep their own,
more detailed SECURITY.md.

## Not inherited

GitHub does NOT inherit some files from the org `.github` repo:

- `LICENSE` — always per-repo, legal reason
- `CONTRIBUTING.md` — actually IS inheritable, but our apps' build
  commands differ enough (xcodebuild flags, scheme names, working
  directories) that we keep CONTRIBUTING.md per-repo
- CI workflows under `.github/workflows/` — not inherited; shared
  CI lives in a separate reusable-workflow repo, invoked via
  `uses:` calls

## Editing

Direct commits to `main` are fine — this repo has no CI gate and
no per-app downstream cascading. For a larger reorganization, use
a short-lived branch off main and merge it back instead.
