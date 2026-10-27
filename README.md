# Robin Baby for Cursor and Grok Bot

Robin Baby is a baby tracker for feeds, sleep, diapers, pumping and more. This plugin connects your Robin Baby account to Cursor and Grok Bot, so you can ask questions about your baby's day and log new events in plain language, for example "How did she sleep last night?" or "Log a 120 ml bottle at 3pm".

## What you need

- A Robin Baby account with an active subscription or free trial. Download the app by searching "Baby Tracker: Robin" on the App Store or Google Play. Subscriptions are only ever billed there, never through an assistant.
- One child per connection. You choose which child to share when you connect.

## Install

1. Install **Robin Baby** from the Cursor Marketplace (Cursor: Settings → Plugins; Grok Bot: Settings → Plugins → Marketplace).
2. Connect the `robin-baby` server. A browser window opens.
3. Sign in to your Robin Baby account, choose which child to share, and approve. You can tick **Read only** if you only want the assistant to read, not log.
4. You land back in your assistant, connected.

Manual setup, without the marketplace: add the server from `mcp.json` in this repository to your own `mcp.json`.

## Sign-in and security

- OAuth 2.1 with PKCE. The client is public, so there is no secret, and `mcp.json` holds only its public client id.
- Nothing can be read until you sign in and approve. The connection reaches only the one child you picked.
- To disconnect, remove the server in your assistant, or email hello@robinbaby.com and we will revoke the connection.

## Tools

Read: `get_baby_profile`, `get_baby_recent_activity`, `count_baby_feeds_sleep_diapers`, `break_down_baby_log`, `compare_baby_log_periods`, `find_baby_log_extremes`, `get_baby_log_streak`, `get_baby_night_wakings`, `get_baby_nap_forecast`, `search_baby_log`, `preview_baby_log_correction`.

Write: `log_baby_event`, `edit_baby_event`, `undo_baby_event`, `apply_baby_log_correction`, `invite_baby_caregiver` (creates an invite code; it sends nothing).

Full tool reference, errors and rate limits: https://www.robinbaby.com/connectors/

## Data and privacy

The tools return, for the one child you connected: their age in months, time zone and feeding profile, a 30-day feeding summary, and the logged events you ask about (times, amounts, durations, your notes and food descriptions). The connector never receives your child's name, date of birth, sex or gestational age, and cannot read growth, allergen, medication, symptom, temperature or vaccination records. Robin Baby does not sell your data. See the Privacy Policy for what we collect, how long we keep it and how to delete it.

- Privacy Policy: https://www.robinbaby.com/privacy/
- Terms: https://www.robinbaby.com/terms/

## Support

hello@robinbaby.com

Robin Baby is a tracking tool, not medical advice. Talk to your pediatrician about your baby's health.
