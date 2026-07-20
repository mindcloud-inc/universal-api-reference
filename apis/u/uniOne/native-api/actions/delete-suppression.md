# Delete Suppression with UniOne

Deletes a suppression from UniOne by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `suppression/delete.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Delete Suppression](https://docs.unione.io/en/web-api-ref#suppression-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to remove from the suppression list. |
