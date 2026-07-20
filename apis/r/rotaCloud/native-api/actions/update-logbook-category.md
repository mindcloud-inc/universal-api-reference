# Update Logbook Category with RotaCloud

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/logbook/categories/:id`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Update Logbook Category](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Logbook category ID. |
| `name` | body | `string` | yes | Logbook category name. |
