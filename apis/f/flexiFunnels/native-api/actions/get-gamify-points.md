# Get Gamify Points with FlexiFunnels

Retrieves gamification points from FlexiFunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/get-gamify-points`
- **Base URL:** `https://bridge.flexifunnels.com`
- **Official documentation:** [Get Gamify Points](https://bridge.flexifunnels.com/docs#gamification-endpoints-POSTapi-get-gamify-points)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `funnel_page_id` | body | `number` | yes |
| `course_id` | body | `number` | yes |
| `lesson_id` | body | `number` | yes |
