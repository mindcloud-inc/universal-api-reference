# Update Contact with WEEEK

## Endpoint

- **Method:** `PATCH`
- **Path:** `/crm/contacts/:contactId`
- **Base URL:** `https://api.weeek.net/public/v1`
- **Official documentation:** [Update Contact](https://developers.weeek.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The WEEEK contact ID from the contacts API. |
| `firstName` | body | `string` | yes | The contact first name. WEEEK required this field during PATCH validation. |
| `lastName` | body | `string` | no | The contact last name. |
| `middleName` | body | `string` | no | The contact middle name. |
| `organizations[]` | body | `array<string>` | no | Optional WEEEK organization IDs to attach to the contact. Send multiple values as a array. |
