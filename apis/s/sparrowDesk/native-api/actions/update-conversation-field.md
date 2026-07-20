# Update Conversation Field with SparrowDesk

Updates an existing conversation field in SparrowDesk.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/conversations/fields/{{id}}`
- **Base URL:** `https://api.sparrowdesk.com/v1`
- **Official documentation:** [Update Conversation Field](https://developer.sparrowdesk.com/rest-api/endpoints/conversations/fields/id/patch)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Updated conversation field description. |
| `id` | path | `number` | yes | SparrowDesk conversation field ID. |
| `is_active` | body | `boolean` | no | Set true to keep the field active. |
| `name` | body | `string` | no | Updated conversation field name. |
| `type` | body | `string` | no | Updated conversation field type. |
