# Update a workflow with Pipedream

Updates an existing workflow in Pipedream.

## Endpoint

- **Method:** `PUT`
- **Path:** `/workflows/{id}`
- **Base URL:** `https://api.pipedream.com/v1`
- **Official documentation:** [Update a workflow](https://pipedream.com/docs/rest-api/api-reference/workflows/update-a-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `active` | body | `boolean` | yes | Set to true to activate the workflow or false to deactivate it. |
| `id` | path | `string` | yes | The workflow identifier. |
| `org_id` | body | `string` | yes | The workspace organization ID that owns the workflow. |
