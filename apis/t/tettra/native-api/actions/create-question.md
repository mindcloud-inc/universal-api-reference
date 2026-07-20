# Create Question with Tettra

Creates a new question in Tettra.

## Endpoint

- **Method:** `POST`
- **Path:** `/teams/85329/questions`
- **Base URL:** `https://app.tettra.co/api`
- **Official documentation:** [Create Question](https://support.tettra.com/api-overview/api-endpoint-create-a-question)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assignees` | body | `list<number>` | no | User IDs to assign the question to. |
| `category_id` | body | `number` | no | Category to ask the question in. |
| `details` | body | `string` | no | Additional question details formatted as HTML. |
| `subcategory_id` | body | `number` | no | Subcategory to ask the question in. |
| `title` | body | `string` | yes | Question title. |
