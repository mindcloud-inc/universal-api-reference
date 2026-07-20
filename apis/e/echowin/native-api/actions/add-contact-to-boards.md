# Add Contact To Boards with echowin

Adds a contact to boards in echowin.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:contactId/boards`
- **Base URL:** `https://echo.win/api/v1`
- **Official documentation:** [Add Contact To Boards](https://echo.win/api-docs/contacts#assign-contact-boards)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactId` | path | `string` | yes |
| `boardIds[]` | body | `array<string>` | yes |
