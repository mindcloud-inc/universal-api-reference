# Set Unsubscribed with UniOne

Adds an email address to UniOne's unsubscribed list.

## Endpoint

- **Method:** `POST`
- **Path:** `unsubscribed/set.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Set Unsubscribed](https://docs.unione.io/en/web-api-ref#unsubscribed-set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | yes | Email address to add to the unsubscribed list. |
