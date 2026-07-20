# List Course Group Participants with CoachAccountable

Retrieves course group participants from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Course Group Participants](https://www.coachaccountable.com/APIDocs#Course.getAllGroupParticipants)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CourseID` | body | `number` | yes | The ID of the Course whose Participants are to be gotten. |
| `GroupID` | body | `number` | no | Optionally filter by ID of the Group for whom Participations are to be gotten. |
| `includeCompleted` | body | `boolean` | no | Include Participants whose Course timeline progression has already been completed. |
