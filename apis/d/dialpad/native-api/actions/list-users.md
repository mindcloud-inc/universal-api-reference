# List Users with Dialpad

Retrieves company user records from Dialpad.

## Endpoint

- **Method:** `GET`
- **Path:** `/users`
- **Base URL:** `https://dialpad.com/api/v2`
- **Official documentation:** [List Users](https://developers.dialpad.com/reference/userslist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | A token used to return the next page of a previous request. Use the cursor provided in the previous response. |
| `state` | query | `string` | no | Filter results by the specified user state. |
| `company_admin` | query | `boolean` | no | If provided, filter results to company admins or non-company admins. |
| `email` | query | `string` | no | The user's email. |
| `number` | query | `string` | no | The user's phone number. |
