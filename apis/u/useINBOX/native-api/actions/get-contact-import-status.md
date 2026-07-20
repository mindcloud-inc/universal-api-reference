# Get Contact Import Status with UseINBOX

Retrieves contact import status from UseINBOX.

## Endpoint

- **Method:** `GET`
- **Path:** `/inbox/v1/contactlists/:contactListId/import/:importId`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Get Contact Import Status](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactListId` | path | `string` | yes | Contact list ID from INBOX. |
| `importId` | path | `string` | yes | Import job ID from INBOX. |
