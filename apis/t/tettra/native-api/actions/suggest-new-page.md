# Suggest New Page with Tettra

Creates a new page suggestion in Tettra.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/85329/suggestions`
- **Base URL:** `https://app.tettra.co/api`
- **Official documentation:** [Suggest New Page](https://support.tettra.com/pages-2/api-endpoint-suggest-a-new-page)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignable_id` | body | `number` | no | User ID to assign the suggestion to. |
| `category` | body | `number` | no | Category to publish the page to. |
| `description` | body | `string` | no | More context about the suggested page. |
| `title` | body | `string` | yes | Suggestion title. |
