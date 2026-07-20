# List Messages with CueGrowth

## Endpoint

- **Method:** `GET`
- **Path:** `/messages`
- **Base URL:** `https://api.cuegrowth.ai/public/api`
- **Official documentation:** [List Messages](https://cuegrowth.ai/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for pagination. |
| `page_size` | query | `number` | no | Page size for pagination. Maximum 100. |
| `sent_date_gt` | query | `date` | no | Filter messages sent after this ISO 8601 datetime. |
| `sent_date_lt` | query | `date` | no | Filter messages sent before this ISO 8601 datetime. |
| `campaigns` | query | `number` | no | Filter messages sent or received by campaign ID. |
| `users` | query | `number` | no | Filter messages sent or received by user ID. |
