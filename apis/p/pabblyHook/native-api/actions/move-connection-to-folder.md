# Move Connection To Folder with Pabbly Hook

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/folders/move-connection`
- **Base URL:** `https://hook.pabbly.com`
- **Official documentation:** [Move Connection To Folder](https://apidocs.pabbly.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionIds[]` | body | `array<string>` | yes | Connection IDs to move. |
| `fromFolderId` | body | `string` | yes | Current folder ID. |
| `toFolderId` | body | `string` | yes | Destination folder ID. |
