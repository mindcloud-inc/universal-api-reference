# List Flashcard Quizzes with LunaNotes

Retrieves flashcard quizzes from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/flashcard-quizzes`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [List Flashcard Quizzes](https://lunanotes.io/docs/flashcard-quizzes/get-v1-flashcard-quizzes)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Comma-separated list of related resources to include. |
| `name` | query | `string` | no | Search quizzes by name using a partial match. |
| `sourceType` | query | `string` | no | Filter by source type such as video, notes, or ai_agent. |
| `videoId` | query | `string` | no | Filter by video ID. |
