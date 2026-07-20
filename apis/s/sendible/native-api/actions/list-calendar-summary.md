# List Calendar Summary with Sendible

## Endpoint

- **Method:** `GET`
- **Path:** `0.1/tw/messages/summary`
- **Base URL:** `https://api.sendible.com`
- **Official documentation:** [List Calendar Summary](https://support.sendible.com/hc/en-us)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | yes | Start datetime in YYYY-MM-DD HH:mm:ss format. |
| `messagesPerDay` | query | `number` | no | Number of messages to include per day. |
| `to` | query | `string` | yes | End datetime in YYYY-MM-DD HH:mm:ss format. |
