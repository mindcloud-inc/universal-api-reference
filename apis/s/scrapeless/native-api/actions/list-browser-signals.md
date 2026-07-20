# List Browser Signals with Scrapeless

Retrieves browser signals from Scrapeless.

## Endpoint

- **Method:** `GET`
- **Path:** `/browser/:taskId/signal/list`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [List Browser Signals](https://apidocs.scrapeless.com/api-24795288)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | session task id |
| `x-api-token` | query | `string` | no | API Key |
