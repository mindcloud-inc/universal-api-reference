# Create Window with Airtop

Creates a new browser window in Airtop.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:sessionId/windows`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Create Window](https://docs.airtop.ai/api-reference/airtop-api/windows/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sessionId` | path | `string` | yes |
| `url` | body | `string` | no |
| `waitUntil` | body | `string` | no |
| `screenResolution` | body | `string` | no |
