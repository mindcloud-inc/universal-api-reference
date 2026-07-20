# Delete Category with SIGNL4

Deletes a category from SIGNL4.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v2/categories/{teamId}/{categoryId}`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Delete Category](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | ID of the team the category belongs to |
| `categoryId` | path | `string` | yes | ID of the category to delete |
