# Junior_Game_QA_portfolio

## 🐞 Bug Report Sample: Game Crash on Loading Screen

**Title:** Game crashes when spamming swipe-back gesture 30+ times on loading screen
**Issue Type:** Bug
**Severity:** High / Critical
**Environment:** 
*   **Device:** POCO M6 Pro (Xiaomi)
*   **OS:** Android 17
*   **Network:** Wi-Fi

**Steps to Reproduce:**
1. Launch the game.
2. Wait for the loading screen to appear.
3. Use the Android system gesture to go back (swipe inward from the right edge of the screen to the left).
4. Swipe once (no message appears).
5. Continue spamming the swipe-back gesture rapidly 30 to 50 times.
6. The "Tap again to exit" message appears.
7. Continue swiping.
8. The game instantly crashes.

**Expected Result:** 
The game should display the exit confirmation message immediately on the first swipe. The game should only close after the player explicitly confirms the exit (e.g., tapping "Yes" or tapping again). It should close cleanly without crashing or causing a re-launch error.

**Actual Result:** 
The game delays the exit message, then crashes ungracefully without a final confirmation. Re-launching the game sometimes takes 1-2 seconds longer, and occasionally displays an error message stating "It couldn't run the game."

**Reproduction Rate:** Intermittent (Occurs sometimes, not 100% every time).

---

## 📋 Test Cases Sample: Loading Screen & Gestures

**Test Case 1: Normal Launch**
*   **Steps:** Launch the game and wait for the loading screen to reach 100%.
*   **Expected Result:** The game successfully transitions to the main menu.
*   **Status:** PASS

**Test Case 2: Single Swipe-Back**
*   **Steps:** Launch the game. While on the loading screen, perform one swipe-back gesture.
*   **Expected Result:** The game displays the exit confirmation immediately and safely returns to the previous menu.
*   **Status:** PASS

**Test Case 3: Spam Swipe-Back (Crash Bug)**
*   **Steps:** Launch the game. While on the loading screen, perform the swipe-back gesture rapidly 30 to 50 times.
*   **Expected Result:** The game should handle the input safely without closing.
*   **Actual Result:** The game crashes instantly.
*   **Status:** FAIL (See Bug Report above)
