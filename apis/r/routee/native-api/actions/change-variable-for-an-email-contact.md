# Change Variable for an Email Contact with Routee

Changes a variable for an email contact in Routee.

## Endpoint

- **Method:** `POST`
- **Path:** `/addressbooks/:addressBookId/emails/variable`
- **Base URL:** `https://connect.routee.net`
- **Official documentation:** [Change Variable for an Email Contact](https://docs.routee.net/reference/testinput-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addressBookId` | path | `string` | yes | ID of the address book containing the necessary email contact with the variable with “name” value |
| `email` | body | `string` | no | email contact, that will have the variable with “name” value changed to “John” |
| `variables[]` | body | `array<object>` | no | array with variables, which is defined by the parameters name (variable name) and value (variable value) |
