# Get Import Status with INBOX

Retrieves an import job status from INBOX.

## Endpoint

- **Method:** `GET`
- **Path:** `/inbox/v1/contactlists/:contactListId/import/:importId`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Get Import Status](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contactListId` | path | `string` | yes |
| `importId` | path | `string` | yes |
