# Get Session Selenium Logs with BrowserStack

Retrieves session Selenium logs from BrowserStack Automate.

## Endpoint

- **Method:** `GET`
- **Path:** `/automate/sessions/:session_id/seleniumlogs`
- **Base URL:** `https://api.browserstack.com`
- **Official documentation:** [Get Session Selenium Logs](https://www.browserstack.com/docs/automate/api-reference/selenium/session#get-session-selenium-logs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_id` | path | `string` | yes | BrowserStack session hashed ID from List Sessions In Build. |
