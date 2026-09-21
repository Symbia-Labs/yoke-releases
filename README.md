# Yoke

An independent macOS controller for the Universal Audio OX Amp Top Box. Every OX in the room on one screen, the whole rig editable in place, the front panel from software or MIDI, all four insert slots on every channel, and an MCP server so an agent can run the box.

This repository holds the downloads and release notes. Yoke's source is not published; the "Source code" archives GitHub attaches to each release contain only this README.

**[Download Yoke for Mac](https://github.com/Symbia-Labs/yoke-releases/releases)** — the newest build is at the top; open the DMG and drag Yoke to Applications.

## Requirements

- macOS 13 or later, Apple Silicon (Intel builds later).
- An OX Amp Top Box on firmware 1.2.0, on the same network as the Mac or reachable by address.

## Installing a beta build

Beta builds are not yet signed or notarized, so macOS refuses the first launch.

1. Open the DMG and drag **Yoke** to Applications.
2. Right‑click Yoke in Applications and choose **Open**, then **Open** again in the dialog. On macOS 15 and later you can instead launch it once, then go to **System Settings → Privacy & Security**, scroll to "Yoke was blocked", and click **Open Anyway**.
3. On first launch macOS asks **"Allow Yoke to find devices on local networks?"** Click **Allow**. Yoke finds OX units with mDNS and talks to them over the LAN; without this it sees nothing.

## Beta terms

Everything in Yoke is free until the end of the beta, the date shown under the gear at the top right → **License** (December 31, 2026). After that Yoke keeps working, and License has a link to buy a key: $9.99, activating up to three Macs. Nothing is locked either way. Please point people at this page rather than passing the DMG on, so they get the newest build.

Builds before 1.0.0-rc.3 stop working on their date; install a newer one from this page.

## Reporting a problem

Click the ⚠ at the top right of the app, describe what happened, and Yoke writes `yoke-report-<time>.zip` to Downloads with its own log, the unit's snapshot and daemon logs, and any macOS crash reports. Nothing is sent automatically. Email the zip to **help@symbia-labs.com**.

## What it never does

Yoke writes only the controls you touch, and every write is read back from the unit. It never changes speaker impedance, saves a preset only when you press Save (over a user preset, or as a new one), never deletes, moves, imports or exports presets, and never touches firmware, passwords or the unit's reset paths. Loading a preset or changing RIG/bank discards unsaved edits on the OX, exactly like turning the physical knob; the app says so before it runs.

---

Yoke is an independent product of Symbia Labs and is not affiliated with or endorsed by Universal Audio. OX and OX Amp Top Box are trademarks of Universal Audio, Inc.
