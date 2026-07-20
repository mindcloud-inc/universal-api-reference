# Add URL Feedback with WebCategorize

## Endpoint

- **Method:** `POST`
- **Path:** `/url/feedback/{urlId}`
- **Base URL:** `https://app.webcategorize.com/api`
- **Official documentation:** [Add URL Feedback](https://webcategorize.com/webcategorize.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlId` | path | `string` | yes | The ID of the URL submission. |
| `score` | body | `number` | yes | Feedback score: 1 for positive feedback, 2 for negative feedback. |
| `language` | body | `string` | no | Language that should have been detected. |
| `classification[]` | body | `array<string>` | no | Category IDs that should have been detected. |
| `comment` | body | `string` | no | Optional feedback comment. |
