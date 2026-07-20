# Scan Uploaded File with Nightfall.ai

Scans an uploaded file with Nightfall.ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/upload/:fileId/scan`
- **Base URL:** `https://api.nightfall.ai`
- **Official documentation:** [Scan Uploaded File](https://help.nightfall.ai/developer-api/key-concepts/file_scan/scan_api_calls)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | The upload UUID to scan. |
| `policy` | body | `object` | yes | Nightfall policy object with webhookURL plus detection rules or detection rule UUIDs. |
| `requestMetadata` | body | `string` | no | Optional metadata echoed back when the asynchronous scan completes. |
