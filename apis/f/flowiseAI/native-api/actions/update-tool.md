# Update Tool with FlowiseAI

Updates an existing tool in FlowiseAI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/tools/{id}`
- **Base URL:** `https://cloud.flowiseai.com/api/v1`
- **Official documentation:** [Update Tool](https://docs.flowiseai.com/api-reference/tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | no | JSON body with documented Flowise tool fields to update. |
| `id` | path | `string` | yes | Tool ID to update. |
