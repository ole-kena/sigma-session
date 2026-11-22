SIGMA SESSION V2 — UPDATED PWA BUILD

Included in this update:
- V2-only project; original V1 is not modified.
- Removed the displayed logo and tagline. V2 is smaller than the app name.
- Removed the Killzone adjustment/settings panel.
- Replaced the old three Killzone windows with the five ICT windows from the supplied ICT Trading Windows & Sessions PDF:
  Asian Killzone: 19:00–22:00 New York
  London Open: 02:00–05:00 New York
  New York AM: 07:00–10:00 New York
  London Close: 10:00–12:00 New York
  NY PM: 13:00–16:00 New York
- Added session tracking based on page 1 of the supplied PDF:
  Asian Session: 18:00–00:00 New York
  London Session: 01:00–12:00 New York
  New York AM Session: 08:00–12:00 New York
  New York PM Session: 13:00–16:30 New York
- Dashboard now shows Active Session and Next Session.
- Added animated gold timelines and live countdowns for market open/close, active Killzone, next Killzone, active Session and next Session.
- Market closed mode counts down to the next market open; market open mode counts down to weekly close.
- Integrated automatic US economic-calendar fetching through Finance Calendar API. Save an API key in the Calendar tab. The app refreshes hourly while open and also supports manual refresh.
- Calendar displays Ethiopia time (Africa/Addis_Ababa), event impact, and actual/forecast/previous values when supplied by the selected API plan.
- Removed manual event-entry UI and unnecessary descriptive copy.
- Kept the integrated lot-size calculator and original app navigation.

ECONOMIC CALENDAR SETUP:
1. Create an API account/key at https://www.financecalendar.com/api/
2. Paste the key into the Calendar tab and press SAVE KEY.
3. The API requires a key. Free Developer access is schedule-only, limited to 100 successful schedule responses per month / 10 per day, next 7 days, max 20 events per response, and does not include numerical actual/forecast/previous values. Paid plans add numerical fields. Review the provider's current terms and prices before choosing a plan.
4. The calendar uses US events with high and medium impact. It is a Forex Factory-style calendar experience, but the data provider is Finance Calendar, not Forex Factory. Do not treat this as an official Forex Factory feed.

ALARM LIMITATION:
- PWA notifications can alert when the app is running and notification permission is granted.
- A browser/PWA cannot guarantee scheduled notifications when the app/browser is fully closed or Android suspends it.
- Reliable closed-app Android alarms still require the native Capacitor/Android implementation and device-level testing. This ZIP is still a PWA, not an APK.

MARKET HOURS:
- The weekly XAUUSD open/close times remain a common estimate (Sunday 17:00 to Friday 17:00 New York). Broker schedules vary; verify against the XAUUSD symbol specification in your broker's MT5.
- All ICT windows are interpreted in America/New_York time so EDT/EST shifts are handled automatically.
- The supplied PDF's New York windows are used as written. The PDF shows Ethiopia summer/winter equivalents on page 1.

LOT CALCULATOR:
- XAUUSD = 100 troy ounces per standard lot.
- Listed FX pairs = 100,000 base units per standard lot.
- USD account, rounded down to 0.01 lot steps.
- Broker contract size, tick value, spread, commission and slippage may change actual risk.

TESTING:
- HTML/JavaScript syntax check passed.
- ZIP integrity check passed after packaging.
- This is not yet a complete real-device QA pass. Test the dashboard, timezone/DST transitions, API key connection and alarms on the Galaxy A15 before relying on it.
- Install/host from HTTPS for PWA functionality and service worker support.

The supplied V1 archive remains untouched.
