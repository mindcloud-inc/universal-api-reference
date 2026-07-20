# List Course Client Availabilities with CoachAccountable

Retrieves course client availabilities from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [List Course Client Availabilities](https://www.coachaccountable.com/APIDocs#Course.getAvailabilitiesForClient)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | ID of the Client for whom Course Availabilities are to be gotten. |
| `includeUsed` | body | `boolean` | no | Include Course Availabilities which have already been used. |
