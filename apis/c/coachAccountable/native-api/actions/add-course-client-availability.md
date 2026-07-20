# Add Course Client Availability with CoachAccountable

Adds course client availability in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Add Course Client Availability](https://www.coachaccountable.com/APIDocs#Course.addClientAvailability)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | The ID of the Client to make the Course availabile to. |
| `CourseID` | body | `number` | yes | The ID of the Course that the Client is to have made available. |
| `dateAvailable` | body | `date` | no | A [future] date at which the Client is be able to start the Course. If not supplied (or not in the future) the Course will be made available to the Client immediately. |
