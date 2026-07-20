# Get Flashcard with LunaNotes

Retrieves a flashcard from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/flashcards/:id`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [Get Flashcard](https://lunanotes.io/docs/flashcards/get-v1-flashcards-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The LunaNotes flashcard ID. |
| `include` | query | `string` | no | Comma-separated: video. |
