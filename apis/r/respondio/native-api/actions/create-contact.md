# Create Contact with respond.io

Creates a new contact in respond.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact/:identifier`
- **Base URL:** `https://api.respond.io/v2`
- **Official documentation:** [Create Contact](https://stoplight.io/api/v1/projects/respond/api/nodes/v2/contact-api.yml/paths/~1contact~1%7Bidentifier%7D/post?fromExportButton=true&snapshotType=http_operation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `identifier` | path | `string` | yes | Contact identifier (email: or phone:). |
| `firstName` | body | `string` | yes | Contact first name. |
| `lastName` | body | `string` | no | Contact last name. |
| `phone` | body | `string` | no | Contact phone number in E.164 format. |
| `email` | body | `string` | no | Contact email address. |
| `language` | body | `string` | no | ISO 639-1 language code. |
| `profilePic` | body | `string` | no | Public URL of the contact avatar. |
| `countryCode` | body | `string` | no | ISO 3166-1 alpha-2 country code. |
| `custom_fields[]` | body | `array<object>` | no | Array of custom field updates: [{name, value}]. |
| `custom_fields[].name` | body | `string` | yes | Custom field name (required for each custom field object). |
| `custom_fields[].value` | body | `string` | no | Custom field value for the given custom field name. |
