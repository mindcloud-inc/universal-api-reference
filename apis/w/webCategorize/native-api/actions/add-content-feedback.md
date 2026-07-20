# Add Content Feedback with WebCategorize

## Endpoint

- **Method:** `POST`
- **Path:** `/html/feedback/{contentId}`
- **Base URL:** `https://app.webcategorize.com/api`
- **Official documentation:** [Add Content Feedback](https://webcategorize.com/webcategorize.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contentId` | path | `string` | yes | The ID of the content submission. |
| `score` | body | `number` | yes | Feedback score: 1 for positive feedback, 2 for negative feedback. |
| `language` | body | `string` | no | Language that should have been detected. |
| `classification[]` | body | `array<string>` | no | Category IDs that should have been detected. |
| `comment` | body | `string` | no | Optional feedback comment. |
