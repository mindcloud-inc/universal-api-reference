# Set Client Profile Extra with CoachAccountable

Updates client profile extras in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Set Client Profile Extra](https://www.coachaccountable.com/APIDocs#Client.setProfileExtra)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | — |
| `profileExtra` | body | `string` | no | Any additional information you'd like to have on file, accessible at-a-glance. Maximum length: 2000. |
