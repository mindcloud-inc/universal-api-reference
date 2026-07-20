# Get CRM Entity Item with Uspacy

Retrieves a CRM entity item from Uspacy.

## Endpoint

- **Method:** `GET`
- **Path:** `/crm/v1/entities/:entity/:itemId`
- **Base URL:** `https://{site}`
- **Official documentation:** [Get CRM Entity Item](https://uspacy.readme.io/reference/get_crm-v1-entities-entity-itemid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity` | path | `string` | yes | The CRM entity key. |
| `itemId` | path | `string` | yes | The CRM item ID. |
