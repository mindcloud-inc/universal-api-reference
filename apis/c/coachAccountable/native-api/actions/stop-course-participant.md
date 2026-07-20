# Stop Course Participant with CoachAccountable

Stops a course participant in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Stop Course Participant](https://www.coachaccountable.com/APIDocs#Course.stopParticipant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CourseParticipantID` | body | `number` | yes | The ID of the Participant to be removed. |
| `deleteItems` | body | `boolean` | no | Should already-dispatched Course Items be deleted as well? |
