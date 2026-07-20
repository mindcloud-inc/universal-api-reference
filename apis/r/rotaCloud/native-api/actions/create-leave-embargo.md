# Create Leave Embargo with RotaCloud

Creates a leave embargo in RotaCloud.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/leave_embargoes`
- **Base URL:** `https://api.rotacloud.com`
- **Official documentation:** [Create Leave Embargo](https://rotacloud.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | body | `string` | yes | Embargo end date in ISO format. |
| `start_date` | body | `string` | yes | Embargo start date in ISO format. |
| `users[]` | body | `array<number>` | yes | User IDs covered by the embargo. Send multiple values as a array separated by `,`. |
