# Create Live Lesson with TrainerCentral

Creates a live lesson in TrainerCentral.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions.json`
- **Base URL:** `{academyUrl}/api/v4/{orgId}`
- **Official documentation:** [Create Live Lesson](https://help.trainercentral.com/portal/en/kb/articles/create-a-session)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `session.name` | body | `string` | yes | The name of the live lesson. |
| `session.description` | body | `string` | no | Optional description for the live lesson. |
| `session.courseId` | body | `string` | yes | The course under which the live lesson should be created. |
| `session.sectionId` | body | `string` | yes | The chapter under which the live lesson should be created. |
| `session.scheduledTime` | body | `number` | yes | Live lesson start time in milliseconds. |
| `session.scheduledEndTime` | body | `number` | yes | Live lesson end time in milliseconds. |
| `session.timezone` | body | `string` | yes | IANA timezone for the scheduled start and end times. |
