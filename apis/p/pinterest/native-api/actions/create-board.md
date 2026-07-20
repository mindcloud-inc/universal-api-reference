# Create Board with Pinterest

Creates a new board in Pinterest.

## Endpoint

- **Method:** `POST`
- **Path:** `boards`
- **Base URL:** `https://api.pinterest.com/v5`
- **Official documentation:** [Create Board](https://developers.pinterest.com/docs/api/v5/#operation/boards/create)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | no |
| `description` | body | `string` | no |
| `privacy` | body | `list` | no |
