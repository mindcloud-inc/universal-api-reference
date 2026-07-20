# List Bot Jobs with Cloud BOT

Retrieves bot jobs from Cloud BOT.

## Endpoint

- **Method:** `GET`
- **Path:** `/:public_id/bots/:bot_id/jobs`
- **Base URL:** `https://api.c-bot.pro`
- **Official documentation:** [List Bot Jobs](https://docs.c-bot.pro/wp-content/uploads/2023/09/api-v5-en.html#operation/get-public_id-bots-bot_id-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `public_id` | path | `string` | yes | Public ID of API |
| `bot_id` | path | `string` | yes | BOT ID |
| `limit` | query | `number` | no | Maximum number of jobs to return |
| `sort_order` | query | `string` | no | Sort order asc or desc |
| `statuses` | query | `string` | no | Comma-separated job statuses: 0 succeeded, 1 error, 2 executing |
| `datetime_from` | query | `string` | no | Return jobs created after this ISO 8601 timestamp |
| `datetime_to` | query | `string` | no | Return jobs created before this ISO 8601 timestamp |
| `id_from` | query | `string` | no | Return jobs with IDs greater than this value |
| `id_to` | query | `string` | no | Return jobs with IDs smaller than this value |
| `properties` | query | `string` | no | Comma-separated extra job fields |
