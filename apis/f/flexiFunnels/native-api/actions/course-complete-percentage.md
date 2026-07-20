# Course Complete Percentage with FlexiFunnels

Retrieves course completion percentages from FlexiFunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/completeperc`
- **Base URL:** `https://bridge.flexifunnels.com`
- **Official documentation:** [Course Complete Percentage](https://bridge.flexifunnels.com/docs#lesson-endpoints-POSTapi-completeperc)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `funnel_page_id` | body | `number` | yes |
| `course_id` | body | `number` | yes |
| `lesson_id` | body | `number` | yes |
