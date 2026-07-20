# Fast Forward Course Participant with CoachAccountable

Fast-forwards a course participant in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Fast Forward Course Participant](https://www.coachaccountable.com/APIDocs#Course.fastForwardParticipant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CourseParticipantID` | body | `number` | yes | The ID of the Participant to be fast forwarded. |
| `days` | body | `number` | no | How many days to fast forward? Must be 1 or greater. |
| `dispatchItems` | body | `boolean` | no | Should Course items during the fast-forward period be dispatched to this participant? |
| `issueNotifications` | body | `boolean` | no | IF Course items during the fast-forward period should be dispatched, should notifications of them be sent to this participant? Ignored when dispatchItems is false. |
