# Google Play Console: Data Safety Form Walkthrough for CraftDroid

**Application Name:** CraftDroid  
**Package Name:** `com.example.craftdroid`  
**Target:** Google Play Console > Policy > App Content > **Data Safety**

Use this guide to complete the Google Play Data Safety declaration form. The answers below align with CraftDroid's local-first on-device container architecture, zero developer data collection, Playit.gg network tunneling, and Google AdMob ad integration.

---

## Screen 1: Data Collection & Security

| Question | Recommended Answer | Explanation |
| :--- | :--- | :--- |
| **Does your app collect or share any of the required user data types?** | **Yes** | Even though CraftDroid maintains no developer databases or cloud servers, Google AdMob processes device identifiers for advertising, and Playit.gg routes network traffic for multiplayer. |
| **Is all of the user data collected by your app encrypted in transit?** | **Yes** | All network communications (upstream server engine downloads, Playit tunnels, and AdMob ads) use HTTPS / TLS encrypted protocols. |
| **Do you provide a way for users to request that their data is deleted?** | **Yes** | Users have 100% on-device custody. Users can delete worlds, clear server instances, or uninstall the app to instantly delete all data. |

---

## Screen 2: Data Types Selection

Select only the following categories and data types:

### 1. Device or Other Identifiers
* Check: **Device or other identifiers**
  * *Explanation:* Required for Google Mobile Ads (AdMob) SDK (Google Advertising ID / GAID).

### 2. App Info and Performance
* Check: **Diagnostics** (for Google Mobile Ads SDK).

*(Note: CraftDroid does NOT collect Personal Info, Financial Info, Health, Messages, Photos, Audio, Contacts, or Precise Location).*

---

## Screen 3: Details for Selected Data Types

### Device or Other Identifiers (Google AdMob)
1. **Is this data collected, shared, or both?**
   * Select: **Shared** *(or "Collected" by the Google Mobile Ads SDK)*
2. **Is this data processed ephemerally?**
   * Select: **No**
3. **Is this data required for your app, or can users choose whether it's collected?**
   * Select: **Data collection is required** *(or optional if consent SDK allows refusal in EEA)*
4. **Why is this user data collected/shared?**
   * Check: **Advertising or marketing**
   * Check: **Fraud prevention, security, and compliance**
   * Check: **Analytics**

---

## Screen 4: Financial, Health, Location, and Personal Info
* **Location:** Select **No** (CraftDroid does not access GPS or coarse network location; coarse IP location is used strictly by Google AdMob on the network layer).
* **Personal info (Name, Email, Address, User IDs):** Select **No**.
* **Financial info:** Select **No**.
* **Health and fitness:** Select **No**.
* **Photos and videos / Audio / Files / Contacts:** Select **No**.
* **Messages:** Select **No** (Minecraft player chat remains 100% local on the device and is never transmitted to the developer).

---

## Summary for Privacy Policy URL Field in Play Console
When Google Play Console asks for:
`Policy > App Content > Privacy Policy > Privacy policy URL`

Provide your deployed GitHub Pages URL:
```text
https://thewhitecarp.github.io/CraftDroid.github.io/privacy.html
```
*(Or `https://thewhitecarp.github.io/CraftDroid.github.io/`).*

---

## Screen 5: Foreground Service Declarations (`FOREGROUND_SERVICE`)
When Google Play Console asks for:
`Policy > App Content > Foreground service permissions`

* **Category:** Select **Special Use** (or System / Utility).
* **User-Facing Video / Demonstration:** Demonstrates initiating a Java/Bedrock server, minimizing the app, and verifying that connected players remain in-game without the Android OS killing the background container process.
* **Justification Description:**
  > "CraftDroid hosts local, persistent Minecraft Java and Bedrock game servers on the user's Android device. The Foreground Service runs the multi-threaded JVM container and Playit.gg tunneling daemon, ensuring seamless multiplayer connectivity when the user switches apps or when the screen turns off."
