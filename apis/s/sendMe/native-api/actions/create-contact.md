# Create Contact with SendMe

## Endpoint

- **Method:** `POST`
- **Path:** `/api/contacts`
- **Base URL:** `https://app.sendme123.com`
- **Official documentation:** [Create Contact](https://docs.sendme123.com/en/api/contacts/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `birthDate` | body | `date` | no | Birth date value. |
| `countryCode` | body | `string` | no | Country code (for example 57). |
| `customValues` | body | `object` | no | Custom field values. |
| `email` | body | `string` | no | Contact email address. |
| `lastName` | body | `string` | no | Contact last name. |
| `name` | body | `string` | yes | Contact name. |
| `phone` | body | `string` | yes | Phone number without country prefix. |
| `status` | body | `string` | no | Contact status (ACTIVE, INACTIVE, BLOCKED). |
| `tagIds` | body | `list<string>` | no | Associated tag IDs. |
