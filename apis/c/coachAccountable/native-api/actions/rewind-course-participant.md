# Rewind Course Participant with CoachAccountable

Rewinds a course participant in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Rewind Course Participant](https://www.coachaccountable.com/APIDocs#Course.rewindParticipant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CourseParticipantID` | body | `number` | yes | The ID of the Participant to be rewound. |
| `days` | body | `number` | no | How many days to rewind? Must be 1 or greater. |
| `deleteItems` | body | `boolean` | no | Should Course items during the rewind period be deleted from this participant, so that they may be newly dispatched as the Course progresses the next time around? |
