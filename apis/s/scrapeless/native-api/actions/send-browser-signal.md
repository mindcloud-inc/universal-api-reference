# Send Browser Signal with Scrapeless

Creates a browser signal in Scrapeless.

## Endpoint

- **Method:** `POST`
- **Path:** `/browser/:taskId/signal/send`
- **Base URL:** `https://api.scrapeless.com`
- **Official documentation:** [Send Browser Signal](https://apidocs.scrapeless.com/api-24795286)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | session task id |
| `x-api-token` | query | `string` | no | API Key |
| `event` | body | `string` | yes | Event channel name (1-256 characters) |
| `data` | body | `object` | yes | Event data payload |
