# Get Member Points with FlexiFunnels

Retrieves member points from FlexiFunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/get-member-points`
- **Base URL:** `https://bridge.flexifunnels.com`
- **Official documentation:** [Get Member Points](https://bridge.flexifunnels.com/docs#gamification-endpoints-POSTapi-get-member-points)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `funnel_page_id` | body | `number` | yes |
| `course_id` | body | `number` | yes |
| `lesson_id` | body | `number` | yes |
