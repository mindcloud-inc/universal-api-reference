# Replace Contact Assignments with echowin

Replaces contact assignments in echowin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contactId/assignments`
- **Base URL:** `https://echo.win/api/v1`
- **Official documentation:** [Replace Contact Assignments](https://echo.win/api-docs/contacts#replace-assignments)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactId` | path | `string` | yes |
| `userIds[]` | body | `array<string>` | yes |
