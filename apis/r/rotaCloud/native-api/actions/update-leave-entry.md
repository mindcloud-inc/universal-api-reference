# Update Leave Entry with RotaCloud

Updates a leave record in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/leave/:id`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Update Leave Entry](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Leave entry ID. |
| `type` | body | `number` | yes | Leave type ID. |
| `start_date` | body | `string` | yes | Leave entry start date in YYYY-MM-DD format. |
| `end_date` | body | `string` | yes | Leave entry end date in YYYY-MM-DD format. |
| `users[]` | body | `array<number>` | yes | User IDs on the leave entry. |
| `user` | body | `number` | no | Primary user for leave update headers. |
