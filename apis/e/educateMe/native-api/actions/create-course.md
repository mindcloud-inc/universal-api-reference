# Create Course with EducateMe

Creates a new course in EducateMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/courses`
- **Base URL:** `https://api.educate-me.co`
- **Official documentation:** [Create Course](https://edme.notion.site/API-integration-v0-2-ef33641eb7f24fa9a6efb969c1f2928f#7e8cb7da90ea4766a12238dfe9f8c74d)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Course title. |
| `previewUrl` | body | `string` | yes | Course preview URL. |
| `withProgramSyncing` | body | `boolean` | yes | Whether program syncing is enabled. |
| `type` | body | `string` | yes | Course type. Allowed values: COHORT_BASED, SELF_PACED. Accepted values: `0`, `1`. |
| `duplicatedCourseId` | body | `string` | no | Optional course ID to copy structure from. |
| `instructorEmails[]` | body | `array<string>` | no | Optional instructor emails. |
