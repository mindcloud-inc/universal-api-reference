# List Earnings Events with White Swan

Retrieves earnings events from White Swan.

## Endpoint

- **Method:** `POST`
- **Path:** `/earnings_event`
- **Base URL:** `https://app.whiteswan.io/api/1.1/wf`
- **Official documentation:** [List Earnings Events](https://docs.whiteswan.io/partner-knowledge-base/api-documentation/information-calls/earnings-event-s)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_email` | body | `string` | no | Optionally filter earnings events by client email. |
| `user_email` | body | `string` | no | Optionally filter earnings events by account user email. |
| `lookback` | body | `number` | no | Optionally limit events to the last N days. |
