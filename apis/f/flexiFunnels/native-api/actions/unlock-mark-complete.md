# Unlock Mark Complete with FlexiFunnels

Deletes a lesson completion mark in FlexiFunnels.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/delete-markecomplete`
- **Base URL:** `https://bridge.flexifunnels.com`
- **Official documentation:** [Unlock Mark Complete](https://bridge.flexifunnels.com/docs#lesson-endpoints-POSTapi-delete-markecomplete)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `funnel_page_id` | body | `number` | yes |
| `course_id` | body | `number` | yes |
| `lesson_id` | body | `number` | yes |
