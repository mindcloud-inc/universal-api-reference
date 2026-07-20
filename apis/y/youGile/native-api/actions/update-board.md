# Update board with YouGile

Updates an existing board in YouGile.

## Endpoint

- **Method:** `PUT`
- **Path:** `/boards/:id`
- **Base URL:** `{companyDomain}/api-v2`
- **Official documentation:** [Update board](https://ru.yougile.com/api-v2#/operations/BoardController_update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The YouGile board ID. |
| `title` | body | `string` | no | The updated board title. |
| `projectId` | body | `string` | no | The project that owns the board. |
| `stickers` | body | `object` | no | Updated sticker configuration map for the board. |
| `deleted` | body | `boolean` | no | Mark the board as deleted. |
