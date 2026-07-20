# List Calendar Messages with Sendible

## Endpoint

- **Method:** `GET`
- **Path:** `0.1/tw/messages`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [List Calendar Messages](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | yes | Start datetime in YYYY-MM-DD HH:mm:ss format. |
| `pageSize` | query | `number` | no | Requested page size. |
| `perPage` | query | `number` | no | Requested page size alias. |
| `to` | query | `string` | yes | End datetime in YYYY-MM-DD HH:mm:ss format. |
