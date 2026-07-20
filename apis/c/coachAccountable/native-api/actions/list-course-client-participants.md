# List Course Client Participants with CoachAccountable

Retrieves course client participants from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Course Client Participants](https://www.coachaccountable.com/APIDocs#Course.getAllClientParticipants)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CourseID` | body | `number` | yes | The ID of the Course whose Participants are to be gotten. |
| `ClientID` | body | `number` | no | Optionally filter by ID of the Client for whom Participations are to be gotten. |
| `includeCompleted` | body | `boolean` | no | Include Participants whose Course timeline progression has already been completed. |
