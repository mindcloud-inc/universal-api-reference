# List Course Module Lessons with Mentortools

Retrieves lessons for a course module in Mentortools.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/v1/modules/:module_id/lessons`
- **Base URL:** `https://app.mentortools.com/public_api`
- **Official documentation:** [List Course Module Lessons](https://app.mentortools.com/public_api/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `module_id` | path | `number` | yes | The module ID. |
