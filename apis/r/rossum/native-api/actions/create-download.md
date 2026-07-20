# Create Download with Rossum

Creates a document download in Rossum.

## Endpoint

- **Method:** `POST`
- **Path:** `/documents/downloads`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Create Download](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `documents[]` | body | `array<string>` | yes | List of document URLs to include in the download. |
