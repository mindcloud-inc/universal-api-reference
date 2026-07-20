# Update Contact with echowin

Updates a contact in echowin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contactId`
- **Base URL:** `https://echo.win/api/v1`
- **Official documentation:** [Update Contact](https://echo.win/api-docs/contacts#update-contact)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactId` | path | `string` | yes |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `email` | body | `string` | no |
| `number` | body | `string` | no |
| `carrier` | body | `string` | no |
| `customFields` | body | `object` | no |
| `crmStageId` | body | `string` | no |
| `tagIds[]` | body | `array<string>` | no |
| `tagNames[]` | body | `array<string>` | no |
