# Create Leave Entry with RotaCloud

Creates a leave record in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/leave`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Create Leave Entry](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `users[]` | body | `array<number>` | yes | User IDs receiving the leave entry. |
| `user` | body | `number` | no | Primary user for leave creation headers. |
| `type` | body | `number` | yes | Leave type ID. |
| `start_date` | body | `string` | yes | Leave entry start date in YYYY-MM-DD format. |
| `end_date` | body | `string` | yes | Leave entry end date in YYYY-MM-DD format. |
