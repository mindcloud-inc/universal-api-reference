# List Unsubscribed with UniOne

Retrieves unsubscribed email addresses from UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `unsubscribed/list.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [List Unsubscribed](https://docs.unione.io/en/web-api-ref#unsubscribed-list)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_from` | body | `string` | no | Return unsubscribed emails from this UTC date onward. |
