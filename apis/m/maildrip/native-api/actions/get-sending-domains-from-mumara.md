# Get sending domains from Mumara with Maildrip

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/mumara/sending-domains`
- **Base URL:** `https://api.maildrip.io`
- **Official documentation:** [Get sending domains from Mumara](https://api.maildrip.io/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `number` | no | Specific sending domain ID |
| `user_id` | query | `number` | no | Filter by user ID |
| `limit_start` | query | `number` | no | Starting row for pagination |
| `limit_count` | query | `number` | no | Number of records to return |
