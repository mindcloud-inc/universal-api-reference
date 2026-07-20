# Create board with YouGile

Creates a new board in YouGile.

## Endpoint

- **Method:** `POST`
- **Path:** `/boards`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [Create board](https://ru.yougile.com/api-v2#/operations/BoardController_create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | The board title. |
| `projectId` | body | `string` | yes | The project that owns the board. |
| `stickers` | body | `object` | no | Optional sticker configuration map for the board. |
