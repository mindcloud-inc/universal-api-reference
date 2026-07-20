# Create Contact with Lexware Office

Creates a new contact in Lexware Office.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Create Contact](https://developers.lexware.io/docs/#contacts-endpoint-create-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `version` | body | `number` | yes | The contact version. Set to 0 when creating a new contact. |
| `roles.customer` | body | `object` | no | Pass an empty object to assign the customer role. |
| `roles.vendor` | body | `object` | no | Pass an empty object to assign the vendor role. |
| `company.name` | body | `string` | no | The company name for company contacts. |
| `person.salutation` | body | `string` | no | The person salutation. |
| `person.firstName` | body | `string` | no | The person first name. |
| `person.lastName` | body | `string` | no | The person last name. |
| `note` | body | `string` | no | An internal note for the contact. |
