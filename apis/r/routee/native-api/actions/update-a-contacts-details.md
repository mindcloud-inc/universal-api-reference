# Update a contact's details with Routee

Updates a contact's details in Routee.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/my/:id`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Update a contact's details](https://docs.routee.net/reference/update-a-contacts-details)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the contact to be updated. |
| `labels[]` | body | `array<object>` | no | — |
| `labels[].name` | body | `string` | no | The name of the label. |
| `labels[].value` | body | `string` | no | The value of the label. |
| `email` | body | `string` | no | The e-mail address of the contact. |
| `firstName` | body | `string` | no | The first name of the contact. The length must be between 1 and 60. |
| `lastName` | body | `string` | no | The last name of the contact. The length must be between 1 and 60. |
| `mobile` | body | `string` | yes | The mobile number of the contact. |
| `vip` | body | `boolean` | no | Indicates whether the contact is treated as vip or not. Default value false |
