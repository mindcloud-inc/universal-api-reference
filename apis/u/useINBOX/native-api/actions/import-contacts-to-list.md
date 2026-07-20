# Import Contacts To List with UseINBOX

Imports contacts into a list in UseINBOX.

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/v1/contactlists/:contactlistId/import`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Import Contacts To List](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactlistId` | path | `string` | yes | Contact list ID that will receive the imported contacts. |
| `contacts[]` | body | `array<object>` | yes | Array of contact objects to import. Each object should follow the documented INBOX import shape with email and optional customFields. |
