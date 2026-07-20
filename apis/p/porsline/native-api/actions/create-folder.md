# Create Folder with Porsline

## Endpoint

- **Method:** `POST`
- **Path:** `/api/folders/`
- **Base URL:** `https://survey.porsline.com`
- **Official documentation:** [Create Folder](https://developers.porsline.com/#tag/Folders/paths/~1api~1folders~1/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `order` | body | `number` | no | Folder order. If omitted, Porsline assigns the highest order. |
