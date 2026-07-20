# Create Client with CoachAccountable

Creates a client in CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Create Client](https://www.coachaccountable.com/APIDocs#Client.add)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | yes | Maximum length: 50. |
| `lastName` | body | `string` | yes | Maximum length: 50. |
| `email` | body | `string` | yes | Maximum length: 50. |
| `homePhone` | body | `string` | no | Maximum length: 20. |
| `cellPhone` | body | `string` | no | Maximum length: 20. |
| `workPhone` | body | `string` | no | Maximum length: 20. |
| `gender` | body | `list` | no | Accepted values: `F`, `M`, `U`. |
| `timezone` | body | `string` | no | The timezone of the new Client. If not provided, defaults to match her Coach's timezone. |
| `address` | body | `string` | no | The client's street address. Maximum length: 100. |
| `city` | body | `string` | no | The client's city. Maximum length: 100. |
| `state` | body | `string` | no | The client's state. Maximum length: 3. |
| `ZIP` | body | `string` | no | The client's ZIP or postal code. Maximum length: 10. |
| `onDuplicateEmail` | body | `list` | no | What to do if a Client with the supplied email already exists. Accepted values: `A`, `E`, `S`. |
| `upgradeIfNeeded` | body | `boolean` | no | If alread at the limit, upgrade the account to make space for the new Client. If false, the call will return failure when there is no space. |
| `sendInvite` | body | `boolean` | no | Send true if the new client should be sent an invite email immediately. |
| `inviteSubject` | body | `string` | no | Subject line of the invite email to be sent (if opted for). If not included, will use template setting. |
| `inviteMessage` | body | `string` | no | Body of the invite email to be sent (if opted for], [magicLink] is required. If not included, will use template setting. |
| `profileExtra` | body | `string` | no | Any additional information you'd like to have on file, accessible at-a-glance. Maximum length: 2000. |
| `appointmentScheduleRule` | body | `list` | no | Accepted values: `ABE`, `AUE`, `D`, `NA`. |
