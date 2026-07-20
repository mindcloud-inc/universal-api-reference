# Create Or Update Contact with ContactDrive

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.contactdrive.app/api/v1`
- **Official documentation:** [Create Or Update Contact](https://help.contactdrive.io/article/16-api-v1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data` | body | `object` | no | Contact payload envelope described by the ContactDrive legacy API article |
| `data.addresses[]` | body | `array<object>` | no | Array of contact address objects with type, street, city, state, zip, and country fields |
| `data.customFields` | body | `object` | no | Object of custom field slug keys mapped to contact-specific values |
| `data.emails[]` | body | `array<object>` | no | Array of contact email objects with type, address, and isPrimary fields |
| `data.firstName` | body | `string` | no | Contact first name |
| `data.fullname` | body | `string` | no | Contact full or mailing name |
| `data.gender` | body | `string` | no | Contact gender value; docs say Male or Female |
| `data.id` | body | `string` | no | ContactDrive system ID for updating an existing contact |
| `data.lastName` | body | `string` | no | Contact last name |
| `data.middleName` | body | `string` | no | Contact middle name |
| `data.nickname` | body | `string` | no | Contact nickname |
| `data.organizations[]` | body | `array<object>` | no | Array of contact organization objects with name, jobTitle, and isCurrent fields |
| `data.phones[]` | body | `array<object>` | no | Array of contact phone objects with type, number, and isPrimary fields |
| `data.prefix` | body | `string` | no | Contact name prefix |
| `data.suffix` | body | `string` | no | Contact name suffix |
| `data.tags[]` | body | `array<string>` | no | Array of tags associated with the contact |
| `data.transactionTotal` | body | `number` | no | Sum of contributions, sales, or other transactions for the contact |
| `data.websites[]` | body | `array<object>` | no | Array of contact website objects with name and URL fields |
