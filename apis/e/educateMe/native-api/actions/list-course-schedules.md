# List Course Schedules with EducateMe

Lists course schedules in EducateMe.

## Endpoint

- **Method:** `GET`
- **Path:** `/courses/:courseId/schedules`
- **Base URL:** `https://api.educate-me.co`
- **Official documentation:** [List Course Schedules](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#9f2290b158a34d74885ccb2dbc290e10)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `courseId` | path | `string` | yes |
| `type` | query | `string` | no |
| `startingDate` | query | `string` | no |
| `endingDate` | query | `string` | no |
