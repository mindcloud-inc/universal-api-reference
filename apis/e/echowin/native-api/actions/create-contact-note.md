# Create Contact Note with echowin

Creates a contact note in echowin.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:contactId/notes`
- **Base URL:** `https://echo.win/api/v1`
- **Official documentation:** [Create Contact Note](https://echo.win/api-docs/contacts#create-note)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactId` | path | `string` | yes |
| `note` | body | `string` | yes |
| `type` | body | `string` | no |
