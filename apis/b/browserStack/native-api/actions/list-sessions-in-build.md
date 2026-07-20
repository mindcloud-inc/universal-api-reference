# List Sessions In Build with BrowserStack

Retrieves build session records from BrowserStack Automate.

## Endpoint

- **Method:** `GET`
- **Path:** `/automate/builds/:build_id/sessions.json`
- **Base URL:** `https://api.browserstack.com`
- **Official documentation:** [List Sessions In Build](https://www.browserstack.com/docs/automate/api-reference/selenium/session#get-session-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `build_id` | path | `string` | yes | BrowserStack build hashed ID from List Builds. |
| `limit` | query | `number` | no | Maximum number of sessions to return. |
| `offset` | query | `number` | no | Offset for session list pagination. |
| `status` | query | `string` | no | Session status filter: running, done, timeout, or failed. |
