# Update Contact with Lexware Office

Updates an existing contact in Lexware Office.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/contacts/:id`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Update Contact](https://developers.lexware.io/docs/#contacts-endpoint-update-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Lexware contact ID. |
| `version` | body | `number` | yes | The current contact version for optimistic locking. |
| `roles.customer` | body | `object` | no | Pass an empty object to assign the customer role. |
| `roles.vendor` | body | `object` | no | Pass an empty object to assign the vendor role. |
| `company.name` | body | `string` | no | The company name for company contacts. |
| `person.salutation` | body | `string` | no | The person salutation. |
| `person.firstName` | body | `string` | no | The person first name. |
| `person.lastName` | body | `string` | no | The person last name. |
| `note` | body | `string` | no | An internal note for the contact. |
