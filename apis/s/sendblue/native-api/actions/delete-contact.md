# Delete Contact with Sendblue

Deletes an existing contact from Sendblue.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/contacts/:phone_number`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Delete Contact](https://docs.sendblue.com/api/resources/contacts/methods/delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone_number` | path | `string` | yes | Phone number in E.164 format. |
