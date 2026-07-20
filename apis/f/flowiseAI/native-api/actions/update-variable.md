# Update Variable with FlowiseAI

Updates an existing variable in FlowiseAI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/variables/{id}`
- **Base URL:** `https://cloud.flowiseai.com/api/v1`
- **Official documentation:** [Update Variable](https://docs.flowiseai.com/api-reference/variables)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | no | JSON body with documented Flowise variable fields to update. |
| `id` | path | `string` | yes | Variable ID to update. |
