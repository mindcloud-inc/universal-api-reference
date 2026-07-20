# Create a Directory with Linkbreakers

Creates a new directory in Linkbreakers.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/directories`
- **Base URL:** `https://api.linkbreakers.com`
- **Official documentation:** [Create a Directory](https://linkbreakers.com/help/api/directories)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the directory. |
| `parentDirectoryId` | body | `string` | no | The parent directory ID. |
