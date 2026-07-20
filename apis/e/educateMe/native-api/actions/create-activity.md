# Create Activity with EducateMe

Creates a new activity in EducateMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/activities`
- **Base URL:** `https://api.educate-me.co`
- **Official documentation:** [Create Activity](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#2b7bb560440146b19c99f8c3a33904b4)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `activityDetails.title` | body | `string` | yes |
| `activityDetails.mainHtml` | body | `string` | yes |
| `activityDetails.isDraft` | body | `boolean` | yes |
| `activityDetails.feedbackRequired` | body | `boolean` | yes |
| `activityDetails.type` | body | `string` | yes |
| `courseId` | body | `string` | yes |
| `moduleId` | body | `string` | yes |
