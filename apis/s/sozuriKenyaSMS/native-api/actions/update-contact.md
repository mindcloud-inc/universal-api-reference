# Update Contact with Sozuri (Kenya) SMS

Updates an existing contact in Sozuri.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contactIdOrMobile`
- **Base URL:** `https://sozuri.net/api/v1`
- **Official documentation:** [Update Contact](https://sozuri.net/docs/contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactIdOrMobile` | path | `string` | yes | The contact ID or mobile number to update. |
| `group` | body | `string` | no | The group name to associate with the updated contact. |
| `contact` | body | `object` | yes | The contact fields to update. |
