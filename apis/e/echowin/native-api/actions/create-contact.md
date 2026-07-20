# Create Contact with echowin

Creates a contact in echowin.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://echo.win/api/v1`
- **Official documentation:** [Create Contact](https://echo.win/api-docs/contacts#create-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `email` | body | `string` | no |
| `number` | body | `string` | yes |
| `carrier` | body | `string` | no |
| `customFields` | body | `object` | no |
| `tagIds[]` | body | `array<string>` | no |
| `tagNames[]` | body | `array<string>` | no |
| `note` | body | `object` | no |
| `assignUserIds[]` | body | `array<string>` | no |
| `boardIds[]` | body | `array<string>` | no |
