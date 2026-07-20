# List Courses with TrainerCentral

Retrieves courses from TrainerCentral.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses.json`
- **Base URL:** `{academyUrl}/api/v4/{orgId}`
- **Official documentation:** [List Courses](https://help.trainercentral.com/portal/en/kb/articles/view-all-courses-api)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter` | query | `number` | no | Optional course source filter. Use 1 for public page, 2 for site builder, 3 for API-created, or 4 for mapped courses. |
