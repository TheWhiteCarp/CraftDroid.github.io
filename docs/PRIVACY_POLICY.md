# Privacy Policy for CraftDroid

**Effective Date:** September 27, 2026  
**Application Name:** CraftDroid  
**Application ID / Package:** `com.example.craftdroid`  
**Developer / Publisher:** TheWhiteCarp  
**Contact:** `thewhitecarp@protonmail.com`  

---

> **Mojang Studios Non-Affiliation Disclaimer:**  
> NOT AN OFFICIAL MINECRAFT PRODUCT. NOT APPROVED BY OR ASSOCIATED WITH MOJANG OR MICROSOFT.  
> Minecraft is a registered trademark of Mojang AB / Microsoft Corporation. CraftDroid is an independent third-party server hosting utility developed by TheWhiteCarp.

---

## 1. Introduction & Core Privacy Philosophy
CraftDroid is designed with an uncompromising **local-first, privacy-by-design architecture**. CraftDroid enables users to run, configure, and manage Minecraft Java Edition (PaperMC, PurpurMC, FabricMC) and Minecraft Bedrock Dedicated Servers directly on Android devices utilizing local container runtimes (PRoot and Box64).

* **Zero Developer Data Collection (First-Party):** We do not operate external application servers, central player databases, analytics trackers, or user profiling systems. We do not collect, monetize, log, or transmit personal data, email addresses, IP addresses, or game world files.
* **100% On-Device Local Server Execution:** Minecraft server processes, JVM environments, world saves, player data files, and server properties are executed and stored entirely within your device's private, sandboxed app storage.
* **Third-Party Networking & Advertising:** Optional Playit.gg tunneling allows multiplayer without port forwarding. Google AdMob displays ads in public releases to fund maintenance.

---

## 2. What Information We Do NOT Collect
* **No Personal Identifiers:** No names, emails, phone numbers, or passwords.
* **No World or Gameplay Inspection:** World seeds, map files, inventories, server logs, operator lists (`ops.json`), whitelists, and chat messages are never transmitted to or visible to the developer.
* **No Biometrics or Location:** No GPS location, camera, microphone, or contacts access.
* **No Tracking SDKs:** Zero behavioral tracking or session analytics.

---

## 3. Local Storage, World Custody & Data Retention
* Server runtime files are isolated inside: `/data/data/com.example.craftdroid/files/`.
* Backups and exports use Android's Storage Access Framework (SAF), preserving total user custody.
* Clearing app data or uninstalling the app permanently purges all local servers, configurations, and world saves immediately.

---

## 4. Third-Party Services & Network Data Transits
* **Playit.gg:** Routes incoming multiplayer packets (TCP 25565, UDP 19132) through Playit.gg's edge network. Subject to [Playit.gg Privacy Policy](https://playit.gg/privacy).
* **Google AdMob:** Collects standard device identifiers (GAID) and coarse IP location for ad delivery and fraud prevention under [Google Advertising Privacy](https://policies.google.com/technologies/ads).
* **Upstream Server Downloads:** Official release binaries downloaded directly from PaperMC (`api.papermc.io`), PurpurMC (`api.purpurmc.org`), FabricMC (`meta.fabricmc.net`), Mojang Bedrock CDN, and Adoptium. Only standard HTTP GET requests are performed without telemetry.

---

## 5. Android Device Permissions
* `INTERNET`: Binary downloads, Playit tunneling, and AdMob ads.
* `FOREGROUND_SERVICE` & `FOREGROUND_SERVICE_SPECIAL_USE`: Continuous server operation while backgrounded.
* `POST_NOTIFICATIONS`: Server status and thermal safety alerts.
* `WAKE_LOCK`: Prevents CPU sleep while hosting active players.
* `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS`: Exempts server process from OEM background task termination.

---

## 6. Mojang Studios EULA Compliance
Users must agree that `eula=true` as required by Mojang Studios ([Mojang EULA](https://www.minecraft.net/en-us/eula)). Commercial monetization must follow the [Mojang Commercial Usage Guidelines](https://www.minecraft.net/en-us/usage-guidelines).

---

## 7. Contact Us
* **Developer:** TheWhiteCarp  
* **Email:** `thewhitecarp@protonmail.com`  
* **GitHub Repository:** [https://github.com/TheWhiteCarp/CraftDroid.github.io](https://github.com/TheWhiteCarp/CraftDroid.github.io)  
