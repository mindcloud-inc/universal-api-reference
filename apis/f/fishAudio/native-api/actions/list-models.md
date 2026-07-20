# List Models with Fish Audio

Retrieves voice models from Fish Audio.

## Endpoint

- **Method:** `GET`
- **Path:** `/model`
- **Base URL:** `https://api.fish.audio`
- **Official documentation:** [List Models](https://docs.fish.audio/api-reference/endpoint/model/list-models)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | query | `string` | no | Filter models by title. |
| `tag[]` | query | `array<string>` | no | Filter models by tag. |
| `self` | query | `boolean` | no | When true, return only models created by the authenticated user. |
| `author_id` | query | `string` | no | Filter models by author ID when self is false. |
| `language[]` | query | `array<string>` | no | Filter models by language. |
| `title_language[]` | query | `array<string>` | no | Filter models by title language. |
| `sort_by` | query | `list` | no | Sort models by score, task count, or creation time. Accepted values: `0`, `1`, `2`. |
