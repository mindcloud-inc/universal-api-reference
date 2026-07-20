# Get Article with Helpjuice

Retrieves an article from Helpjuice.

## Endpoint

- **Method:** `GET`
- **Path:** `/articles/:id`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Article](https://help.helpjuice.com/api-v3/using-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The Helpjuice article ID. |
| `processed` | query | `boolean` | no | Return processed_body in the article answer when true. |
| `kb_language` | query | `string` | no | Return the translated article for the requested kb language when available. |
