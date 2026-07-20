# Update List with KiteSuite

Updates an existing list in KiteSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/list/:id`
- **Base URL:** `https://api.kitesuite.com`
- **Official documentation:** [Update List](https://api.kitesuite.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | List ID. |
| `listName` | body | `string` | yes | Updated list name. |
| `status` | body | `string` | yes | Updated list status. |
