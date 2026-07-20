# Create File with Airtop

Creates a new file in Airtop.

## Endpoint

- **Method:** `POST`
- **Path:** `/files`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Create File](https://docs.airtop.ai/api-reference/airtop-api/files/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `fileName` | body | `string` | yes |
| `fileType` | body | `string` | no |
| `sessionIds` | body | `string` | no |
