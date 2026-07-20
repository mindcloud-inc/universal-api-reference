# Create Contact with WEEEK

## Endpoint

- **Method:** `POST`
- **Path:** `/crm/contacts`
- **Base URL:** `https://api.weeek.net/public/v1`
- **Official documentation:** [Create Contact](https://developers.weeek.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emails[]` | body | `array<string>` | no | Optional email addresses for the contact. Send multiple values as a array. |
| `firstName` | body | `string` | yes | The contact first name. |
| `lastName` | body | `string` | no | The contact last name. |
| `middleName` | body | `string` | no | The contact middle name. |
| `organizations[]` | body | `array<string>` | no | Optional WEEEK organization IDs to attach to the contact. Send multiple values as a array. |
| `phones[]` | body | `array<string>` | no | Optional phone numbers for the contact. Send multiple values as a array. |
