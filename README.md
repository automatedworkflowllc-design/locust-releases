# Locust

<p align="center"><a href="https://locust.lol"><img src="assets/locust-banner.png" alt="Locust: AI teammates, on the models you pick" width="100%"></a></p>

Locust runs AI coding teammates against a folder on your machine. You choose
the runtime, the model, and how much each teammate is allowed to do — and you
bring your own accounts, keys or free tiers. It resells nobody's tokens.

This repository carries the installers and the update feed. The source is not
public yet, so **[Issues here](https://github.com/automatedworkflowllc-design/locust-releases/issues)
is the right place for bugs and questions.**

<table>
<tr>
<td><img src="assets/shots/01-home.png" alt="Home screen with six teammates, each on its own AI"><br><sub>Your team. Each teammate keeps its own AI and model.</sub></td>
<td><img src="assets/shots/02-model-picker.png" alt="The model picker with Claude Code and Codex models"><br><sub>One picker for the models your own accounts offer.</sub></td>
</tr>
<tr>
<td><img src="assets/shots/03-run-in-progress.png" alt="A teammate working, with its plan card"><br><sub>Watch a teammate work, plan and all.</sub></td>
<td><img src="assets/shots/04-approval.png" alt="An approval card before a command runs"><br><sub>In Approve each, nothing runs until you have seen the exact command and where it runs.</sub></td>
</tr>
<tr>
<td><img src="assets/shots/05-hand-off.png" alt="A hand-off chain where a checker on a different AI approves"><br><sub>Hand-off chains: Wren (OpenCode) diagnoses, Atlas (Codex) checks the code and approves.</sub></td>
<td><img src="assets/shots/06-finished.png" alt="The finished change with its diff and a new test"><br><sub>The change, the diff and the new test, right in the thread.</sub></td>
</tr>
</table>

<sub>Screenshots from 0.437 and 0.438 on a demo profile. The models in the picker are what that account offers; yours come from your own accounts.</sub>

## What a teammate is

A teammate is a name, a role and a route — a runtime and a model you picked.
Give one a folder and a job and it works there, and the whole run is written
to a local ledger you can reopen.

They are not separate chat windows. A teammate can hand work to another one
by name, and the reply comes back into the conversation that asked; each
answers on its own route, so you can put two models on the same problem and
see both. A **Chief of Staff** takes what you asked for, gives it to the
teammate whose role fits, and reports back in one message. Conversations can
be grouped, and a group's standing instructions brief every turn from the
moment you put a conversation in it.

A **hand-off chain** is a routine whose steps go to different teammates, each
on its own runtime, with a checker that must approve before the run counts.
Each runtime's own `/` commands are in the menu (Claude Code, OpenCode, Codex),
`@` attaches a project file, and up to eight runs can go at once.

Deleting a conversation is undoable — the record waits in **Settings → Trash**
until you empty it.

## Install

Download **`Locust-Setup.exe`** from the
[latest release](https://github.com/automatedworkflowllc-design/locust-releases/releases/latest)
and run it. That name is version-stable and always the newest build, which is
what [locust.lol](https://locust.lol) links; the `Locust-<version>-setup.exe`
beside it is the same bytes under a name that says which build it is.

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
not. It carries its own npm for that, so you do not need Node.js installed.
(A first install on a machine that has never had Node has not yet been tested
from scratch; if it fails for you, please file it.)

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
