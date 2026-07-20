# Check In Participant with Sympla

Checks in a participant in Sympla by participant ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/events/:eventId/participants/:participantId/checkin`
- **Base URL:** `https://api.sympla.com.br/public/v1.5.1`
- **Official documentation:** [Check In Participant](https://developers.sympla.com.br/api-doc/index.html#operation/checkInByParticipantId)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `eventId` | path | `string` | yes | Unique identifier of the event. |
| `participantId` | path | `number` | yes | Unique identifier of the participant ticket to check in. |
