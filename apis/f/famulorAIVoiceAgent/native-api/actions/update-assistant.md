# Update Assistant with Famulor AI - Voice Agent

Updates an existing AI assistant in Famulor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/user/assistant/:id`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Update Assistant](https://docs.famulor.io/en/api-reference/assistants/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Famulor assistant ID. |
| `language_id` | body | `number` | no | Language ID for the assistant. |
| `name` | body | `string` | no | Assistant display name. |
| `voice_id` | body | `number` | no | Voice ID for the assistant. |
