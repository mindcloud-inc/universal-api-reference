# Take Screenshot with Airtop

Takes a screenshot of an Airtop window.

## Endpoint

- **Method:** `POST`
- **Path:** `/sessions/:sessionId/windows/:windowId/screenshot`
- **Base URL:** `https://api.airtop.ai/api/v1`
- **Official documentation:** [Take Screenshot](https://docs.airtop.ai/api-reference/airtop-api/windows/screenshot)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `sessionId` | path | `string` | yes |
| `windowId` | path | `string` | yes |
