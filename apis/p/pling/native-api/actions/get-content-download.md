# Get Content Download with Pling

Retrieves a content download URL from Pling.

## Endpoint

- **Method:** `GET`
- **Path:** `/content/download/:contentId/:itemId`
- **Base URL:** `https://api.pling.com/ocs/v1`
- **Official documentation:** [Get Content Download](https://www.opendesktop.org/ocs-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contentId` | path | `string` | yes | Pling content identifier to download from. |
| `itemId` | path | `string` | yes | Download item number for the content entry. |
