# Submit Feedback with ScrapeGraphAI

Submits rating feedback for a ScrapeGraphAI request.

## Endpoint

- **Method:** `POST`
- **Path:** `/feedback`
- **Base URL:** `https://api.scrapegraphai.com/v1`
- **Official documentation:** [Submit Feedback](https://docs.scrapegraphai.com/api-reference/endpoint/user/submit-feedback)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `feedback_text` | body | `string` | no | Optional free-form feedback text. |
| `rating` | body | `number` | yes | Rating value from 0 to 5. |
| `request_id` | body | `string` | yes | Request ID the feedback refers to. |
