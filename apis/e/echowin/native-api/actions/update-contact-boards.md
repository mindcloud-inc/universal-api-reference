# Update Contact Boards with echowin

Updates contact boards in echowin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contacts/:contactId/boards`
- **Base URL:** `https://echo.win/api/v1`
- **Official documentation:** [Update Contact Boards](https://echo.win/api-docs/contacts#update-contact-boards)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactId` | path | `string` | yes |
| `boardIds[]` | body | `array<string>` | yes |
