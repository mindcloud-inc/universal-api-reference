# Get Website Status with Mallabe

Retrieves website status details from Mallabe.

## Endpoint

- **Method:** `POST`
- **Path:** `/websites/status`
- **Base URL:** `https://mallabe.p.rapidapi.com/v1`
- **Official documentation:** [Get Website Status](https://app.mallabe.com/websites/status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `website` | body | `string` | yes | Website URL to check. |
| `method` | body | `string` | yes | HTTP method to use for the website check. |
| `webhookUrl` | body | `string` | no | Webhook URL for asynchronous callbacks. |
