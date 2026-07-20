# Update Knowledge Base with Famulor AI - Voice Agent

Updates an existing knowledge base in Famulor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/user/knowledgebases/:id`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Update Knowledge Base](https://docs.famulor.io/en/api-reference/knowledgebases/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Knowledge base description. |
| `id` | path | `number` | yes | Famulor knowledge base ID. |
| `name` | body | `string` | no | Knowledge base name. |
