# Create Contact with PostGrid Print & Mail

Creates a contact in PostGrid Print & Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.postgrid.com/print-mail/v1`
- **Official documentation:** [Create Contact](https://postgrid.readme.io/reference/contacts_create-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | no | The first name for the contact recipient. |
| `companyName` | body | `string` | no | The company name for the contact recipient. |
| `lastName` | body | `string` | no | The last name for the contact recipient. |
| `addressLine1` | body | `string` | yes | The first line of the contact address. |
| `addressLine2` | body | `string` | no | The second line of the contact address, if applicable. |
| `city` | body | `string` | no | The city for the contact address. |
| `provinceOrState` | body | `string` | no | The province or state for the contact address. |
| `postalOrZip` | body | `string` | no | The postal or ZIP code for the contact address. |
| `countryCode` | body | `string` | yes | The ISO 3166-1 country code for the contact address. |
| `email` | body | `string` | no | The email address for the contact. |
| `phoneNumber` | body | `string` | no | The phone number for the contact. |
| `jobTitle` | body | `string` | no | The job title for the contact. |
| `skipVerification` | body | `boolean` | no | Skip PostGrid address verification for this contact. |
| `forceVerifiedStatus` | body | `boolean` | no | Force the contact address status to verified. |
| `description` | body | `string` | no | An optional description visible in the API and dashboard. |
| `metadata` | body | `object` | no | Custom metadata for this contact. |
