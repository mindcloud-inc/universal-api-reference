# Create Or Update Contact with respond.io

Finds a contact in respond.io, or creates one if no match is found.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/create_or_update/:identifier`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [Create Or Update Contact](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1create_or_update~1%7Bidentifier%7D/post?fromExportButton=true&snapshotType=http_operation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Contact identifier (id:, email:, or phone:). |
| `firstName` | body | `string` | no | Contact first name. |
| `lastName` | body | `string` | no | Contact last name. |
| `phone` | body | `string` | no | Contact phone number in E.164 format. |
| `email` | body | `string` | no | Contact email address. |
| `language` | body | `string` | no | ISO 639-1 language code. |
| `profilePic` | body | `string` | no | Public URL of the contact avatar. |
| `countryCode` | body | `string` | no | ISO 3166-1 alpha-2 country code. |
| `custom_fields[]` | body | `array<object>` | no | Array of custom field updates: [{name, value}]. |
| `custom_fields[].name` | body | `string` | yes | Custom field name (required for each custom field object). |
| `custom_fields[].value` | body | `string` | no | Custom field value for the given custom field name. |
