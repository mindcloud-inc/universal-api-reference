# Update Contact with Salesmate

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact/v4/:contactId`
- **Base URL:** `https://apis.salesmate.io`
- **Official documentation:** [Update Contact](https://apidocs.salesmate.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `number` | yes | Salesmate contact ID. |
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
