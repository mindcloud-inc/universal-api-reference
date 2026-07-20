# Parse User Agent with Mallabe

Retrieves parsed user agent details from Mallabe.

## Endpoint

- **Method:** `POST`
- **Path:** `/uas/parse`
- **Base URL:** `https://mallabe.p.rapidapi.com/v1`
- **Official documentation:** [Parse User Agent](https://app.mallabe.com/user-agents/parse/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userAgent` | body | `string` | yes | User agent string to parse. |
| `webhookUrl` | body | `string` | no | Webhook URL for asynchronous callbacks. |
