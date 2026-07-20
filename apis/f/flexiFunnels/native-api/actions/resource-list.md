# Resource List with FlexiFunnels

Retrieves lesson resources from FlexiFunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/downloadcontent`
- **Base URL:** `https://bridge.flexifunnels.com`
- **Official documentation:** [Resource List](https://bridge.flexifunnels.com/docs#lesson-endpoints-POSTapi-downloadcontent)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `funnel_page_id` | body | `number` | yes |
| `course_id` | body | `number` | yes |
| `lesson_id` | body | `number` | yes |
