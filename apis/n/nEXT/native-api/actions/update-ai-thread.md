# Update AI Thread with NEXT

Updates an existing AI thread in NEXT.

## Endpoint

- **Method:** `PUT`
- **Path:** `/ai-threads/:id`
- **Base URL:** `https://rest.eu-west-1.nextapp.co/v1`
- **Official documentation:** [Update AI Thread](https://developer.nextapp.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The AI thread ID. |
| `name` | body | `string` | yes | Updated AI thread name. |
