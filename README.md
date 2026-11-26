# Server apps: downloads

The newest builds of Spoty, Glance and Butterfly. This page is rewritten by the Release workflow in `server-apps`
on every build; nothing here is edited by hand.

| App | Android | iPhone | Mac (Apple silicon) |
| --- | --- | --- | --- |
| Spoty | [Download APK 1.0.135](https://github.com/hamuelpalallos/server-apps-release/releases/download/build-135/spoty-135.apk) (92 MB) | 1.0.135 via SideStore / AltStore ([IPA](https://github.com/hamuelpalallos/server-apps-release/releases/download/build-135/spoty-135.ipa), 10 MB) | [Download for Mac 1.0.131](https://github.com/hamuelpalallos/server-apps-release/releases/download/build-131/spoty-131.dmg) (20 MB) |
| Glance | [Download APK 1.0.135](https://github.com/hamuelpalallos/server-apps-release/releases/download/build-135/glance-135.apk) (89 MB) | 1.0.135 via SideStore / AltStore ([IPA](https://github.com/hamuelpalallos/server-apps-release/releases/download/build-135/glance-135.ipa), 10 MB) | — |
| Butterfly | [Download APK 1.0.135](https://github.com/hamuelpalallos/server-apps-release/releases/download/build-135/butterfly-135.apk) (88 MB) | 1.0.135 via SideStore / AltStore ([IPA](https://github.com/hamuelpalallos/server-apps-release/releases/download/build-135/butterfly-135.ipa), 10 MB) | — |

- **Android:** open the APK link on your phone and tap Install. After that the app updates itself (it asks when a
  new build is out; Settings → Check for updates checks right away).
- **Mac:** open the .dmg and drag Spoty to Applications. The first time, macOS says it can't check the app: open
  System Settings → Privacy & Security → Open Anyway. After that Spoty updates itself (Spoty → Check for Updates…).
- **iPhone:** add this source once in AltStore or SideStore, then install and update the apps from there:
  `https://cdn.jsdelivr.net/gh/hamuelpalallos/server-apps-release@main/altstore-source.json`
  See [iPhone setup with a free Apple ID](#iphone-setup-with-a-free-apple-id) below.
- [All releases](https://github.com/hamuelpalallos/server-apps-release/releases) ·
  [updates.json](https://raw.githubusercontent.com/hamuelpalallos/server-apps-release/main/updates.json) (what the apps read)

## iPhone setup with a free Apple ID

No paid Apple Developer account needed. AltStore signs the apps with your own Apple ID, and AltServer on an
always-on Mac (the Mac mini) keeps them signed.

1. **On the Mac:** install AltServer from [altstore.io](https://altstore.io) (AltStore Classic). It sits in the menu
   bar. If it asks to install the Mail plug-in, follow its steps.
2. **Connect the iPhone by USB** and tap Trust. In Finder, select the iPhone and turn on *Show this iPhone when on
   Wi-Fi*, so AltServer can reach it later without the cable.
3. **Install AltStore:** AltServer menu → Install AltStore → your iPhone, and sign in with your Apple ID (any Apple
   ID works; a spare one is fine).
4. **On the iPhone:**
   - Settings → General → VPN & Device Management → your Apple ID → Trust.
   - iOS 16 and later: Settings → Privacy & Security → Developer Mode → on (the iPhone restarts).
5. **Add the source:** open AltStore → Sources → + and paste
   `https://cdn.jsdelivr.net/gh/hamuelpalallos/server-apps-release@main/altstore-source.json`.
   Then install Spoty, Glance or Butterfly from Browse.

**Free Apple ID limits:**
- **Three apps at a time, and AltStore is one of them**, so two of Spoty, Glance and Butterfly at once. To swap,
  deactivate one in My Apps; its data stays.
- **Apps expire after 7 days unless refreshed.** AltStore refreshes them in the background whenever the iPhone and
  the Mac running AltServer are on the same Wi-Fi. You can also open AltStore → My Apps → Refresh All. If an app
  does expire, refresh it and it opens again with its data intact.
- **At most 10 new app IDs per 7 days.** Normal updates don't use one up.

**Updates:** AltStore shows new builds under My Apps → Updates. The apps also check by themselves and send you to
AltStore when a new build is out.

**Without a computer:** SideStore (sidestore.io) does the same job and refreshes on the iPhone itself, using a small
on-device VPN. It needs a computer once for setup. The same source URL works there.
