# Pause Course Participant with CoachAccountable

Pauses a course participant in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Pause Course Participant](https://www.coachaccountable.com/APIDocs#Course.pauseParticipant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CourseParticipantID` | body | `number` | yes | The ID of the Participant to be paused. |
| `unpauseDate` | body | `date` | no | Date at which the Participant is to resume the Course. Omit to pause indefinitely. |
