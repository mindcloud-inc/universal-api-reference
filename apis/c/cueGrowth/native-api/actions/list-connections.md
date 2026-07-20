# List Connections with CueGrowth

## Endpoint

- **Method:** `GET`
- **Path:** `/connections`
- **Base URL:** `https://api.cuegrowth.ai/public/api`
- **Official documentation:** [List Connections](https://cuegrowth.ai/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for pagination. |
| `page_size` | query | `number` | no | Page size for pagination. Maximum 100. |
| `creation_date_gt` | query | `date` | no | Filter connections after this ISO 8601 datetime. |
| `creation_date_lt` | query | `date` | no | Filter connections before this ISO 8601 datetime. |
| `receiver_username` | query | `string` | no | Filter connections to a receiver with this LinkedIn username. |
| `receiver_first_name` | query | `string` | no | Filter connections to a receiver with this first name. |
| `receiver_last_name` | query | `string` | no | Filter connections to a receiver with this last name. |
| `campaigns` | query | `number` | no | Filter by campaign ID. |
| `users` | query | `number` | no | Filter by user ID. |
| `campaign_types` | query | `string` | no | Filter connections by campaign type. |
| `clicked_only` | query | `boolean` | no | Filter connections that clicked the tracking link. |
| `connection_date_lt` | query | `date` | no | Filter connections before this ISO 8601 datetime. |
| `connection_date_gt` | query | `date` | no | Filter connections after this ISO 8601 datetime. |
