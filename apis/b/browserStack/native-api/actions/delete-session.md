# Delete Session with BrowserStack

Deletes an existing session from BrowserStack Automate.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/automate/sessions/:session_id.json`
- **Base URL:** `https://api.browserstack.com`
- **Official documentation:** [Delete Session](https://www.browserstack.com/docs/automate/api-reference/selenium/session#delete-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_id` | path | `string` | yes | BrowserStack hashed session ID. |
