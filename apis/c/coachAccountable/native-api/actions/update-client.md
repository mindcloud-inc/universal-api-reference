# Update Client with CoachAccountable

Updates a client in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Update Client](https://www.coachaccountable.com/APIDocs#Client.update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | yes | — |
| `firstName` | body | `string` | no | Maximum length: 50. |
| `lastName` | body | `string` | no | Maximum length: 50. |
| `homePhone` | body | `string` | no | Maximum length: 20. |
| `cellPhone` | body | `string` | no | Maximum length: 20. |
| `workPhone` | body | `string` | no | Maximum length: 20. |
| `timezone` | body | `string` | no | The timezone of the Client. |
| `address` | body | `string` | no | The client's street address. Maximum length: 100. |
| `city` | body | `string` | no | The client's city. Maximum length: 100. |
| `state` | body | `string` | no | The client's state. Maximum length: 3. |
| `ZIP` | body | `string` | no | The client's ZIP or postal code. Maximum length: 10. |
| `appointmentScheduleRule` | body | `list` | no | Accepted values: `ABE`, `AUE`, `D`, `NA`. |
