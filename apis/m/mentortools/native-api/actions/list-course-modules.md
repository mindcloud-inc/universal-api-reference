# List Course Modules with Mentortools

Retrieves modules for a course in Mentortools.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/v1/:course_id/modules`
- **Base URL:** `https://app.mentortools.com/public_api`
- **Official documentation:** [List Course Modules](https://app.mentortools.com/public_api/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `course_id` | path | `number` | yes | The course ID. |
