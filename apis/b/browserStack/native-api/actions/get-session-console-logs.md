# Get Session Console Logs with BrowserStack

Retrieves session console logs from BrowserStack Automate.

## Endpoint

- **Method:** `GET`
- **Path:** `/automate/sessions/:session_id/consolelogs`
- **Base URL:** `https://api.browserstack.com`
- **Official documentation:** [Get Session Console Logs](https://www.browserstack.com/docs/automate/api-reference/selenium/session#get-session-console-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_id` | path | `string` | yes | BrowserStack session hashed ID from List Sessions In Build. |
