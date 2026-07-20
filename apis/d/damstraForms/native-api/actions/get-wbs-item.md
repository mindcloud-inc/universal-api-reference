# Get WBS Item with Damstra Forms

Retrieves a WBS item from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/wbs_items/{id}`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get WBS Item](https://sammapi.docs.apiary.io/#reference/wbs-items/wbs-item-instance/get-a-wbs-item)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The unique id (numeric) or uuid (string) identifier of the project. |
| `id` | path | `number` | yes | The unique identifier of the WBS item. |
