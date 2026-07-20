# Get Flashcard Quiz with LunaNotes

Retrieves a flashcard quiz from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/flashcard-quizzes/:id`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [Get Flashcard Quiz](https://lunanotes.io/docs/flashcard-quizzes/get-v1-flashcard-quizzes-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The LunaNotes flashcard quiz ID. |
| `include` | query | `string` | no | Comma-separated: video,flashcards,scores,notes. |
