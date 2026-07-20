# Add Contact Assignments with echowin

Adds contact assignments in echowin.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:contactId/assignments`
- **Base URL:** `https://echo.win/api/v1`
- **Official documentation:** [Add Contact Assignments](https://echo.win/api-docs/contacts#add-assignments)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactId` | path | `string` | yes |
| `userIds[]` | body | `array<string>` | yes |
