# Create Chapter with TrainerCentral

Creates a new chapter in TrainerCentral.

## Endpoint

- **Method:** `POST`
- **Path:** `/sections.json`
- **Base URL:** `{academyUrl}/api/v4/{orgId}`
- **Official documentation:** [Create Chapter](https://help.trainercentral.com/portal/en/kb/articles/create-a-chapter)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `section.courseId` | body | `string` | yes | The course ID the chapter belongs to. |
| `section.name` | body | `string` | yes | The chapter name. |
