# Update CRM Entity Item with Uspacy

Updates an existing CRM entity item in Uspacy.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/crm/v1/entities/:entity/:itemId`
- **Base URL:** `https://{site}`
- **Official documentation:** [Update CRM Entity Item](https://uspacy.readme.io/reference/patch_crm-v1-entities-entity-itemid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity` | path | `string` | yes | The CRM entity key. |
| `itemId` | path | `string` | yes | The CRM item ID. |
