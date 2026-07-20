# Get Webhook with UniOne

Retrieves a webhook from UniOne by URL.

## Endpoint

- **Method:** `POST`
- **Path:** `webhook/get.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Get Webhook](https://docs.unione.io/en/web-api-ref#webhook-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook URL to look up. |
