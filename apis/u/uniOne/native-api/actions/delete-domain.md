# Delete Domain with UniOne

Deletes an existing domain from UniOne.

## Endpoint

- **Method:** `POST`
- **Path:** `domain/delete.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Delete Domain](https://docs.unione.io/en/web-api-ref#domain-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Domain name to delete. |
