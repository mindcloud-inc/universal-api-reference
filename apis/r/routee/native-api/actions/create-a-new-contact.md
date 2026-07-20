# Create a new contact with Routee

Creates a new contact in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/my`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Create a new contact](https://docs.routee.net/reference/create-a-new-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `labels[]` | body | `array<object>` | no | Contains the contact's labels with their respective values. |
| `labels[].name` | body | `string` | no | The name of the label. |
| `labels[].value` | body | `string` | no | The value of the label. |
| `email` | body | `string` | no | The e-mail address of the contact. |
| `firstName` | body | `string` | no | The first name of the contact. The length must be between 1 and 60. |
| `lastName` | body | `string` | no | The last name of the contact. The length must be between 1 and 60. |
| `mobile` | body | `string` | yes | The mobile number of the contact. |
| `vip` | body | `boolean` | no | Indicates whether the contact is treated as vip or not. Default value false |
