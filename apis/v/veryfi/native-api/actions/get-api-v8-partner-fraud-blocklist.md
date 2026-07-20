# Get devices from blocklist with Veryfi

Retrieves blocked devices from Veryfi.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v8/partner/fraud/blocklist`
- **Base URL:** `https://api.veryfi.com`
- **Official documentation:** [Get devices from blocklist](https://docs.veryfi.com/api/get-devices-from-blocklist/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Default value: 1 The page number. The response is capped to maximum of 50 results per page. |
| `page_size` | query | `number` | no | Default value: 1000 The number of results per page. |
