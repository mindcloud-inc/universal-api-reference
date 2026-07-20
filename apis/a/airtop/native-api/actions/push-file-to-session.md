# Push File To Session with Airtop

Pushes a file to one or more Airtop sessions.

## Endpoint

- **Method:** `POST`
- **Path:** `/files/:fileId/push`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Push File To Session](https://docs.airtop.ai/api-reference/airtop-api/files/push)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileId` | path | `string` | yes |
| `sessionIds` | body | `string` | no |
