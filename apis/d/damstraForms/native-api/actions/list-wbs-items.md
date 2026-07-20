# List WBS Items with Damstra Forms

Retrieves project WBS items from Damstra Forms.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/wbs_items`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [List WBS Items](https://sammapi.docs.apiary.io/#reference/wbs-items/wbs-item-collection/get-a-list-of-project-wbs-items)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | The unique id (numeric) or uuid (string) identifier of the project. |
