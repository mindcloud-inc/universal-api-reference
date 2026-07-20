# Create Company Contact with Streamtime

## Endpoint

- **Method:** `POST`
- **Path:** `/companies/:company_id/contacts`
- **Base URL:** `https://api.streamtime.net/v2`
- **Official documentation:** [Create Company Contact](https://api.streamtime.net/v2/swagger#/Companies/createCompanyContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | path | `number` | yes | Company ID |
| `firstName` | body | `string` | no | First name |
| `lastName` | body | `string` | no | Last name |
| `email` | body | `string` | no | Email address |
| `phoneNumber` | body | `string` | no | Phone number |
| `position` | body | `string` | no | Position or job title |
| `contactStatus` | body | `object` | no | Status of a contact |
| `contactStatus.id` | body | `number` | yes | Contact status ID |
| `contactLabels[]` | body | `array<object>` | no | Labels applied to the contact |
