# Locust

Locust runs AI coding teammates against a folder on your machine. You choose
the runtime, the model, and how much each teammate is allowed to do — and you
bring your own accounts, keys or free tiers. It resells nobody's tokens.

This repository carries the installers and the update feed. The source is not
public yet, so **[Issues here](https://github.com/automatedworkflowllc-design/locust-releases/issues)
is the right place for bugs and questions.**

## Install

Download `Locust-<version>-setup.exe` from the
[latest release](https://github.com/automatedworkflowllc-design/locust-releases/releases/latest)
and run it.

**Windows x64 only today.** macOS and Linux exist in the build configuration
but are not published, so if you are not on Windows there is nothing here you
can run yet. That is a real gap rather than an oversight, and it is the first
thing an outside tester said about this page.

The build is **unsigned**. Windows SmartScreen will show a blue *"Windows
protected your PC"* panel the first time — choose **More info → Run anyway**.
Signing is deliberately not set up for a pre-release, so expect that warning
on every fresh install until it is.

## What you need besides the app

Locust drives coding CLIs; it does not bundle one. On first launch it shows
which CLIs are already on your machine and offers to install the ones that are
not. Most install through npm, so you will want
[Node.js](https://nodejs.org) if you do not have it — without it, that screen
can only tell you what is missing.

The model itself still comes from somewhere you control: your own
subscription, an API key, or a provider's free tier. "Free" here means a free
tier or a local model. It never means unmetered access to a paid plan.

## Updates

The app asks this repository for the latest release when it launches and
installs the update when you quit. `latest.yml` is the feed it reads; the
installer and its blockmap sit beside it in every release. Each release's
notes say what changed.

## Status

Pre-release, and it behaves like one. It is being tested in the open, and the
release notes are written to be honest about what is fixed and what is not.
If something is wrong, please file it — a report from someone who was not
expecting the bug is worth more than any amount of self-testing.
