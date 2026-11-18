# discord-voice-bot-pycord

A maintained packaging fork for [discord-voice-bot](https://github.com/lordmitrii/discord-voice-bot).
This is not an official Pycord release. Upstream authorship and MIT notices are preserved.

Based on Pycord commit `10a5e8cf13bd8db21f95baf62cf866056d1e1091` from upstream PR #3159.
The runtime code is unchanged except for its distribution version lookup. Packaging includes
all nested voice-receive modules. The Python import namespace remains `discord`.

Install in a fresh virtual environment with `pip install "discord-voice-bot-pycord[voice]==0.1.0"`.
Do not install alongside `py-cord`, `discord.py`, or `discord`: they share that namespace.

## Maintenance

Record the upstream commit and review its diff before updating. Retain license notices.
Build and test wheel and source installs on Python 3.11–3.13 and run the bot regression tests.
Bump the fork version independently from upstream. Review upstream security changes regularly.

## Release

Register the PyPI project and a Trusted Publisher for this repository's `voicebot-release.yml`
workflow and `pypi` environment. Configure required reviewers on that environment.
Run the workflow manually with the version confirmed. It builds, validates, and smoke-tests the
artifacts before the protected publish job. Publishing is never triggered by a normal push.
