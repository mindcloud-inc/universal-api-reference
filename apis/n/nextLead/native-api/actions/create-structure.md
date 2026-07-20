# Create Structure with NextLead

Creates a new structure in NextLead.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/receive/structure/new-structure`
- **Base URL:** `https://dashboard.nextlead.app`
- **Official documentation:** [Create Structure](https://dashboard.nextlead.app/en/api-documentation#receive-structure-create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Structure name. |
| `siret` | body | `string` | no | Optional 14-digit structure identifier used for deletion and lookup. |
