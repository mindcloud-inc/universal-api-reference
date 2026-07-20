# Finish File Upload with Nightfall.ai

Finishes a file upload in Nightfall.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/upload/:fileId/finish`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Finish File Upload](https://help.nightfall.ai/developer-api/key-concepts/file_scan/scan_api_calls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | The upload UUID to finish. |
