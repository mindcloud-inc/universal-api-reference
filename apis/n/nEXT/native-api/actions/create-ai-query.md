# Create AI Query with NEXT

Creates a new AI query in NEXT.

## Endpoint

- **Method:** `POST`
- **Path:** `/ai-queries`
- **Base URL:** `https://rest.eu-west-1.nextapp.co/v1`
- **Official documentation:** [Create AI Query](https://developer.nextapp.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `thread_id` | body | `string` | yes | The AI thread that will contain the query. |
| `prompt` | body | `string` | yes | The AI query prompt. |
