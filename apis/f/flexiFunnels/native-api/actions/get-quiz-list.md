# Get Quiz List with FlexiFunnels

Retrieves quizzes from FlexiFunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/quiz-list`
- **Base URL:** `https://bridge.flexifunnels.com`
- **Official documentation:** [Get Quiz List](https://bridge.flexifunnels.com/docs#quiz-endpoints-POSTapi-quiz-list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `funnel_page_id` | body | `number` | yes |
| `course_id` | body | `number` | yes |
| `lesson_id` | body | `number` | yes |
