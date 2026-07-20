# Get Session Logs with BrowserStack

Retrieves session logs from BrowserStack Automate.

## Endpoint

- **Method:** `GET`
- **Path:** `/automate/sessions/:session_id/logs`
- **Base URL:** `https://api.browserstack.com`
- **Official documentation:** [Get Session Logs](https://www.browserstack.com/docs/automate/api-reference/selenium/session#get-session-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_id` | path | `string` | yes | BrowserStack session hashed ID from List Sessions In Build. |
