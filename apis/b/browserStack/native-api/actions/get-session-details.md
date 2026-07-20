# Get Session Details with BrowserStack

Retrieves session details from BrowserStack Automate.

## Endpoint

- **Method:** `GET`
- **Path:** `/automate/sessions/:session_id.json`
- **Base URL:** `https://api.browserstack.com`
- **Official documentation:** [Get Session Details](https://www.browserstack.com/docs/automate/api-reference/selenium/session#get-session-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_id` | path | `string` | yes | BrowserStack session hashed ID from List Sessions In Build. |
