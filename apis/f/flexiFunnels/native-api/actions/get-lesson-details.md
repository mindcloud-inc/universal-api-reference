# Get Lesson Details with FlexiFunnels

Retrieves lesson details from FlexiFunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/lesson-details`
- **Base URL:** `https://bridge.flexifunnels.com`
- **Official documentation:** [Get Lesson Details](https://bridge.flexifunnels.com/docs#lesson-endpoints-POSTapi-lesson-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `funnel_page_id` | body | `number` | yes | Membership course page identifier. |
| `course_id` | body | `number` | yes | Course identifier. |
| `lesson_id` | body | `number` | yes | Lesson identifier. |
