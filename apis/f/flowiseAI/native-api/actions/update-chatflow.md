# Update Chatflow with FlowiseAI

Updates an existing chatflow in FlowiseAI.

## Endpoint

- **Method:** `PUT`
- **Path:** `/chatflows/{id}`
- **Base URL:** `https://cloud.flowiseai.com/api/v1`
- **Official documentation:** [Update Chatflow](https://docs.flowiseai.com/api-reference/chatflows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | no | JSON body with documented chatflow fields to update. |
| `id` | path | `string` | yes | Chatflow ID to update. |
