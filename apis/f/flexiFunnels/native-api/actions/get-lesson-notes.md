# Get Lesson Notes with FlexiFunnels

Retrieves lesson notes from FlexiFunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/get-lesson-notes`
- **Base URL:** `https://bridge.flexifunnels.com`
- **Official documentation:** [Get Lesson Notes](https://bridge.flexifunnels.com/docs#lesson-endpoints-POSTapi-get-lesson-notes)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `funnel_page_id` | body | `number` | yes |
| `course_id` | body | `number` | yes |
| `lesson_id` | body | `number` | yes |
