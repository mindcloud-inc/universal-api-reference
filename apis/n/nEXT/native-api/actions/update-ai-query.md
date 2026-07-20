# Update AI Query with NEXT

Updates an existing AI query in NEXT.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ai-queries/:id`
- **Base URL:** `https://rest.eu-west-1.nextapp.co/v1`
- **Official documentation:** [Update AI Query](https://developer.nextapp.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The AI query ID. |
| `thread_id` | body | `string` | yes | Updated AI thread ID for the query. |
| `prompt` | body | `string` | yes | Updated AI query prompt. |
