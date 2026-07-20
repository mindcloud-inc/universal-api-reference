# List Files with ActiveMerge

Retrieves files and folders for the authenticated user from ActiveMerge.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/files`
- **Base URL:** `https://app.activemerge.com`
- **Official documentation:** [List Files](https://app.activemerge.com/api/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | no | Optional parent folder ID to list files from. |
