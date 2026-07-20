# Mark Complete with FlexiFunnels

Marks a lesson complete in FlexiFunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/markecomplete`
- **Base URL:** `https://bridge.flexifunnels.com`
- **Official documentation:** [Mark Complete](https://bridge.flexifunnels.com/docs#lesson-endpoints-POSTapi-markecomplete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `funnel_page_id` | body | `number` | yes |
| `course_id` | body | `number` | yes |
| `lesson_id` | body | `number` | yes |
