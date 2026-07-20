# Update Contact with SendMe

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/contacts/:id`
- **Base URL:** `https://app.sendme123.com`
- **Official documentation:** [Update Contact](https://docs.sendme123.com/en/api/contacts/update/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `birthDate` | body | `date` | no | Birth date. |
| `countryCode` | body | `string` | no | Country code. |
| `customValues` | body | `object` | no | Custom field values. |
| `email` | body | `string` | no | Contact email address. |
| `id` | path | `string` | yes | Unique contact ID. |
| `lastName` | body | `string` | no | Contact last name. |
| `phone` | body | `string` | no | Phone number. |
| `status` | body | `string` | no | Contact status. |
| `tagIds` | body | `list<string>` | no | Tag IDs to associate. |
