# Clear Browser Signals with Scrapeless

Deletes browser signals from Scrapeless.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/browser/:taskId/signal/clear`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [Clear Browser Signals](https://apidocs.scrapeless.com/api-24795290)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | session task id |
| `x-api-token` | query | `string` | no | API Key |
| `event` | body | `string` | no | Event name, if not provided, all events will be cleared |
