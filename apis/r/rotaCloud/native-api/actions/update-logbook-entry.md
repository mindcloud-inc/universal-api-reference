# Update Logbook Entry with RotaCloud

## Endpoint

- **Method:** `PUT`
- **Path:** `/v2/logbook/:id`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Update Logbook Entry](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Logbook entry ID. |
| `name` | body | `string` | yes | Logbook entry name. |
| `description` | body | `string` | yes | Logbook entry description. |
| `categoryId` | body | `number` | yes | Logbook category ID. |
| `date` | body | `string` | yes | Entry date in YYYY-MM-DD format. |
| `userId` | body | `number` | yes | User ID for the logbook entry. |
| `time` | body | `string` | no | Entry time in HH:mm format. |
