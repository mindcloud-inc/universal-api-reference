# Stop Browser Session with Browser Use

Stops a browser session in Browser Use.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/browsers/:session_id`
- **Base URL:** `https://api.browser-use.com/api/v3`
- **Official documentation:** [Stop Browser Session](https://docs.browser-use.com/cloud/api-v3/browsers/update-browser-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `action` | body | `list` | yes | Browser session update action. Use stop. Accepted values: `0`. |
| `session_id` | path | `string` | yes | Browser session ID. |
