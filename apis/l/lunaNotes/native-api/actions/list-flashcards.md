# List Flashcards with LunaNotes

Retrieves flashcards from LunaNotes.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/flashcards`
- **Base URL:** `https://api.lunanotes.io`
- **Official documentation:** [List Flashcards](https://lunanotes.io/docs/flashcards/get-v1-flashcards)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Comma-separated list of related resources to include. |
| `quizId` | query | `string` | no | Filter by quiz ID. |
| `videoId` | query | `string` | no | Filter by video ID. |
