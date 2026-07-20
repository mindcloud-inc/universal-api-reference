# Update Engagement with CoachAccountable

Updates an engagement in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Update Engagement](https://www.coachaccountable.com/APIDocs#Engagement.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `EngagementID` | body | `number` | yes | — |
| `name` | body | `string` | no | — |
| `startDate` | body | `date` | no | — |
| `endDate` | body | `date` | no | If provided but set to an empty or otherwise invalid date, the Engagement will be set to continue indefinitely. |
| `allocation` | body | `string` | no | The new allocation of the Engagement expressed as a number followed by a space followed by the unit, either "A" for Appointments or "H" for hours (e.g. "12 A" or "6 H"). |
