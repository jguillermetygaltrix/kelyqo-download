# Pulsar

Voice, webcam and screen sharing for small groups — without the memory tax.

Made by [Galtrix](https://galtrixtech.com). Windows app.

## Download

Grab the latest `Pulsar-win-x64.zip` from **[Releases](../../releases)**, unzip
it anywhere, and run **Pulsar.exe**.

The zip holds two files: the app and this guide. Nothing to install, no account,
no sign-up, no email. It does not need .NET or Node — everything it uses is
inside the executable.

The first launch takes a few seconds longer while the app unpacks itself. Every
launch after that is immediate.

Windows may warn that the app is from an unknown publisher the first time. That
is because it is not code-signed yet; choose **More info → Run anyway**.

## Joining a room

Someone sends you an invite that looks like this:

```
PULSAR-eyJoIjoiMTkyLjE2OC4wLjQ2OjM...
```

Paste it into the **Invite code** box on the Pulsar start screen. It fills in
the room for you and shows which machine you are joining. Type your name and
press **Join room**.

## Hosting a room (the person everyone joins)

One person hosts; everyone else joins them. To host, open **Settings** (the gear
icon) and switch on **Let friends join this machine**. Pulsar restarts and
becomes reachable on your local network, protected by a room password it
generates for you.

Then join a room and press **Copy invite** — send that code to whoever you want
in. The invite carries the address, the room and the password together, so they
only have to paste one thing.

Leave the switch off and Pulsar is completely private: nothing outside your own
computer can reach it. That is the default, and it stays that way until you
change it.

**The first time you host, Windows Defender Firewall will ask whether to allow
Pulsar.** Say yes, and tick **Private networks**. If you dismissed that prompt,
Windows quietly created a block rule and nobody will be able to connect.

## In a call

| Button | What it does |
|---|---|
| **Mic** | Mute and unmute. You join muted-safe — the icon always matches reality. |
| **Cam** | Camera, off by default so nothing is running that you did not ask for. |
| **Stream** | Share a window or your whole screen, like Discord's Go Live. |
| **Leave** | Ends the call and releases your mic and camera. |

**Wear headphones if you share system audio.** Sharing the sound of a call
re-broadcasts the call itself, and microphone echo cancellation cannot help —
it never touches your system audio.

## What to know before you join

- **Only join rooms from people you know.** Pulsar connects everyone directly to
  each other, so the people in a room can see each other's IP addresses. That is
  how peer-to-peer calling works and it is not something an invite hides.
- **Treat an invite like a password.** Anyone holding it can join that room.
- **Your video and audio are always encrypted** in transit between people.
- Rooms hold up to 8 people. Chat is live only — nothing is stored anywhere.

## Trouble

**"Camera unavailable — another app is using it."** Something else has the
camera open. Elgato Camera Hub, OBS, Zoom and Teams all hold it exclusively.
Close it and press Cam again.

**Friends cannot reach you.** Windows Defender Firewall shows a prompt the first
time; if it was dismissed, it silently created a block rule. Allow Pulsar on
Private networks.

---

This page only hosts the download. Issues and questions:
[open an issue](../../issues).
