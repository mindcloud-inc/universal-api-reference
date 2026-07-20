# List Inboxes with CueGrowth

## Endpoint

- **Method:** `GET`
- **Path:** `/inbox`
- **Base URL:** `https://api.cuegrowth.ai/public/api`
- **Official documentation:** [List Inboxes](https://cuegrowth.ai/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for pagination. |
| `page_size` | query | `number` | no | Page size for pagination. Maximum 100. |
| `creation_date_gt` | query | `date` | no | Filter inboxes created after this ISO 8601 datetime. |
| `creation_date_lt` | query | `date` | no | Filter inboxes created before this ISO 8601 datetime. |
| `receiver_username` | query | `string` | no | Filter inboxes to a receiver with this LinkedIn username. |
| `receiver_first_name` | query | `string` | no | Filter inboxes to a receiver with this first name. |
| `receiver_last_name` | query | `string` | no | Filter inboxes to a receiver with this last name. |
| `campaigns` | query | `number` | no | Filter messages sent or received by campaign ID. |
| `users` | query | `number` | no | Filter messages sent or received by user ID. |
