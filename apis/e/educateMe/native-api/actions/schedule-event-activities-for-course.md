# Schedule Event Activities for Course with EducateMe

Schedules event activities for a course in EducateMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/courses/:courseId/schedule-events`
- **Base URL:** `https://api.educate-me.co`
- **Official documentation:** [Schedule Event Activities for Course](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#1bf447e2efaa8031a82ef9f1f2daa11d)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `courseId` | path | `string` | yes |
| `scheduleData[]` | body | `array<object>` | yes |
| `isInZoom` | body | `boolean` | yes |
| `zoomAccountEmail` | body | `string` | no |
| `customWebinarRoomLink` | body | `string` | no |
