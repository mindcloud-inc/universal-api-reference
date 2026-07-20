# Edit Structure with NextLead

Updates an existing structure in NextLead.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/receive/structure/edit-structure`
- **Base URL:** `https://dashboard.nextlead.app`
- **Official documentation:** [Edit Structure](https://dashboard.nextlead.app/en/api-documentation#receive-structure-edit)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Structure identifier. |
| `email` | body | `string` | yes | Updated structure email address. |
