# Add Contact with Salesmate

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/v4`
- **Base URL:** `https://apis.salesmate.io`
- **Official documentation:** [Add Contact](https://apidocs.salesmate.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | no | Contact first name. |
| `lastName` | body | `string` | yes | Contact last name. |
| `email` | body | `string` | no | Primary email address. |
| `mobile` | body | `string` | no | Mobile phone number. |
| `owner` | body | `number` | yes | Salesmate user ID that owns the contact. |
| `company` | body | `number` | no | Existing company ID linked to the contact. |
| `designation` | body | `string` | no | Job title or role. |
| `website` | body | `string` | no | Website URL. |
| `description` | body | `string` | no | Internal description for the contact. |
| `tags` | body | `string` | no | Comma-separated tag list. |
