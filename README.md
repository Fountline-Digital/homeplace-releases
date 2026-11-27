# Homeplace

**Where the family comes home to.** Homeplace is a family calendar, chore chart,
meal planner and photo frame for a touchscreen on your wall, fridge or counter.
There's no subscription. It runs on a small Raspberry Pi computer in your home,
and everyone can open it on their phone too.

Made by [Fountline Digital](https://fountlinedigital.com) · [homeplace.fountlinedigital.com](https://homeplace.fountlinedigital.com)

---

## Contents

- [What you need](#what-you-need)
- [Download](#download)
- [Set up a new display](#set-up-a-new-display)
- [First-time setup on the screen](#first-time-setup-on-the-screen)
- [Use it on your phone](#use-it-on-your-phone)
- [Add your calendars](#add-your-calendars)
- [Add photos](#add-photos)
- [Updates](#updates)
- [Backups](#backups)
- [Try it on a Windows PC](#try-it-on-a-windows-pc)
- [Questions and fixes](#questions-and-fixes)
- [Getting help](#getting-help)

---

## What you need

| | |
|---|---|
| **Computer** | Raspberry Pi 5 (2 GB or more). A Raspberry Pi 4 works too. |
| **Screen** | Any HDMI or Raspberry Pi touchscreen. 10" or bigger works best. A screen without touch works with a mouse. |
| **Memory card** | A microSD card, 16 GB or bigger. |
| **Power** | The official Raspberry Pi power supply, or your screen's supply if it powers the Pi. |
| **Another computer** | Only once, to copy Homeplace onto the memory card. |
| **Wi-Fi** | Your home Wi-Fi name and password. |

## Download

Open the **[latest release](../../releases/latest)** and download the file you need:

| File | What it's for |
|---|---|
| `homeplace-<version>-pi.img.xz` | **Most people want this one.** Everything for a new display, ready to copy onto a memory card. |
| `homeplace-<version>-android.apk` | The Homeplace phone app for Android, if it isn't on Google Play for you yet. |
| `homeplace-<version>-win-x64.exe` | Try Homeplace on a Windows PC. |
| `homeplace_<version>_arm64.deb` | Add Homeplace to a Raspberry Pi that's already set up (advanced). |

The other files (`manifest.json`, `manifest.sig`, Linux programs) are used by
automatic updates. You don't need them.

## Set up a new display

1. **Install Raspberry Pi Imager** on your computer from
   [raspberrypi.com/software](https://www.raspberrypi.com/software/).
2. Put the microSD card in your computer and open **Raspberry Pi Imager**.
3. **Device:** pick your Raspberry Pi model.
   **Operating system:** scroll down and pick **Use custom**, then choose the
   `homeplace-…-pi.img.xz` file you downloaded.
   **Storage:** pick your microSD card.
4. Click **Next**. When it asks about **OS customisation**, choose **No**.
   Homeplace does its own setup on the screen.
5. Wait for it to write and check the card (about 5–10 minutes), then take the
   card out.
6. Put the card in the Pi, connect the screen, and plug in power.

The first start takes a minute or two. Then Homeplace opens full screen by itself.

## First-time setup on the screen

Homeplace walks you through it:

1. **Wi-Fi:** tap your network, type the password, tap **Connect**.
   (If the Pi is plugged in with a network cable, this step is skipped.)
2. **Family name:** for example "The Parkers".
3. **Logo:** pick a style made from your name, or tap **Upload** and scan the
   code with your phone to send your own picture.
4. **Family members:** add everyone and give each person a color.
5. **Look:** pick a theme. You can make your own colors later in
   ⚙ Settings → Appearance.

The time zone and weather location are set automatically from your internet
connection.

**Set a parent PIN** in ⚙ Settings → Parent PIN, so kids can't change settings.

## Use it on your phone

Your phone has to be on the **same Wi-Fi** as the display.

**The Homeplace app** (recommended)
- **iPhone:** App Store → search **Homeplace App** *(coming soon)*.
- **Android:** Google Play → **Homeplace App** *(coming soon)*, or download the
  `.apk` from the [latest release](../../releases/latest) and open it. Android
  asks you to allow installing from your browser the first time.
- Open the app. It finds your display on the Wi-Fi by itself. If it doesn't,
  type the address shown on the display in ⚙ Settings → About
  (like `http://192.168.1.50:8080`).

**Or use your phone's browser.** Type the address from ⚙ Settings → About.
- **iPhone (Safari):** Share → **Add to Home Screen**.
- **Android (Chrome):** ⋮ → **Add to Home screen**.

**Away from home?** In ⚙ Settings → Extensions, turn on 🌐 Remote access. Open
it, tap **Install Tailscale**, then scan the code with your phone and sign in to
a free Tailscale account. Put the Tailscale app on your phone with the same
account, and Homeplace opens from anywhere.

## Add your calendars

⚙ Settings → **Calendars**

- **Google Calendar (recommended):** tap **Sign in with Google**, then scan the
  code on the screen with your phone's camera and sign in with your Google
  account. The display finishes connecting by itself. Then tap
  **+ Add a Google calendar** for each calendar and pick who it belongs to.
  Changes show up right away, and events you add on the display go into Google.
- **iPhone/iCloud, Outlook or others:** tap **+ Add calendar link** and paste the
  calendar's share link. The settings page shows how to find the link for each
  one. These calendars are read-only and can take a few hours to update.

Homeplace only shows your calendars and the photos you pick on your own
display. See the [privacy policy](https://homeplace.fountlinedigital.com/privacy).

## Add photos

Open the **Photos** tab (🖼️):

- **From your phone:** point your phone's camera at the code on the Photos tab
  and pick pictures. In the phone app, tap **Choose pictures** instead.
- **Google Photos:** sign in with Google, tap **Pick photos**, and choose them in
  Google Photos.
- **Immich:** if your family runs Immich, connect it in ⚙ Settings → Photos and
  pick the albums to show.

The slideshow starts by itself after a few minutes without a touch.

## Updates

Homeplace checks for updates on its own. When one is ready, a note shows on the
screen: tap **Update now** (it asks for the parent PIN), or **Later**.

- Updates take about a minute, and the screen reloads by itself. **Don't unplug
  it during an update.**
- Your family's information is backed up first. If an update ever fails to
  start, Homeplace goes back to the version you had.
- Every update is checked against Fountline Digital's signature before it
  installs, so nobody else can send one.
- You can check by hand in ⚙ Settings → Updates.

You never need to re-download or re-flash the memory card to update.

## Backups

Homeplace saves a backup every night and before every update. In
⚙ Settings → Backup you can:

- **Download** a backup to your phone or computer (keep one somewhere safe).
- **Restore** a backup, including onto a brand-new display.
- Copy backups to a network folder automatically.

## Try it on a Windows PC

Download `homeplace-…-win-x64.exe` and double-click it. It opens in your web
browser. Your information is saved in `%LOCALAPPDATA%\Homeplace`.

Windows may show **"Windows protected your PC"** because the program isn't
signed yet. Click **More info → Run anyway**.

## Questions and fixes

**The screen is black or shows the desktop instead of Homeplace.**
Wait two minutes after plugging it in. Still nothing? Unplug the power for 10
seconds and plug it back in.

**My phone can't find the display.**
- Make sure the phone is on the same Wi-Fi as the display (not a guest network,
  and not using mobile data).
- Type the address from ⚙ Settings → About by hand.
- Some routers keep devices apart ("client isolation" or "AP isolation"). Turn
  that off in your router's settings.

**I changed my Wi-Fi.**
Plug a network cable into the Pi, or connect a keyboard. Then go to
⚙ Settings → 📶 Wi-Fi on the screen and pick the new network.

**Google calendars stopped showing.**
Go to ⚙ Settings → Calendars. If it asks you to sign in again (this happens if
you changed your Google password or removed access), tap **Sign in with Google**.

**I forgot the parent PIN.**
Connect a keyboard to the display and press **Ctrl + Alt + T** to open a
terminal. Type `sudo homeplace --reset-pin`, press Enter, then type
`sudo systemctl restart homeplace`. Set a new PIN in ⚙ Settings.

**The screen should turn off at night.**
⚙ Settings → Display & sleep → Night mode.

**Can I start over?**
⚙ Settings → About → **Run first-time setup again**. To erase everything, flash the
memory card again. Download a backup first if you want to keep anything.

**Does Homeplace send my family's information anywhere?**
No. Everything stays on your display. Homeplace only goes online to check the
weather, read the calendars and photos you connect, and look for updates.

## Getting help

Contact Fountline Digital at [fountlinedigital.com](https://fountlinedigital.com).
Privacy policy: [homeplace.fountlinedigital.com/privacy](https://homeplace.fountlinedigital.com/privacy).
Tell us the version (⚙ Settings → About) and what you see on the screen. A
photo of the screen helps a lot.
