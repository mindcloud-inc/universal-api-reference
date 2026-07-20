# Set Session Status with BrowserStack

Updates a session status in BrowserStack Automate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/automate/sessions/:session_id.json`
- **Base URL:** `https://api.browserstack.com`
- **Official documentation:** [Set Session Status](https://www.browserstack.com/docs/automate/api-reference/selenium/session#set-test-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session_id` | path | `string` | yes | BrowserStack hashed session ID. |
| `status` | body | `string` | yes | BrowserStack session outcome: passed or failed. Accepted values: `0`, `1`. |
| `reason` | body | `string` | no | Reason text, typically used when marking a session failed. |
