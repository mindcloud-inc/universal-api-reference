# Delete Structure with NextLead

Deletes an existing structure from NextLead.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/receive/structure/delete-structure`
- **Base URL:** `https://dashboard.nextlead.app`
- **Official documentation:** [Delete Structure](https://dashboard.nextlead.app/en/api-documentation#receive-structure-delete)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siret` | body | `string` | yes | Structure SIRET used to delete the structure. |
