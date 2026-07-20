# Member Reward List with FlexiFunnels

Retrieves member rewards from FlexiFunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/member-reward-list`
- **Base URL:** `https://bridge.flexifunnels.com`
- **Official documentation:** [Member Reward List](https://bridge.flexifunnels.com/docs#gamification-endpoints-POSTapi-member-reward-list)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `funnel_page_id` | body | `number` | yes |
| `course_id` | body | `number` | yes |
| `lesson_id` | body | `number` | yes |
