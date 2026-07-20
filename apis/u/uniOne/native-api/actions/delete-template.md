# Delete Template with UniOne

Deletes an email template from UniOne by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `template/delete.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [Delete Template](https://docs.unione.io/en/web-api-ref#template-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Template identifier to delete. |
