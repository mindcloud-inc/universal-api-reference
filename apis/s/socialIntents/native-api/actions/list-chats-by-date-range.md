# List Chats By Date Range with Social Intents

Retrieves chats from Social Intents using a date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/chats`
- **Base URL:** `https://www.socialintents.com/v1/api`
- **Official documentation:** [List Chats By Date Range](https://www.socialintents.com/docs/integrations/rest-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_from` | query | `string` | yes | Start date in YYYY-MM-DD format. |
| `date_to` | query | `string` | yes | End date in YYYY-MM-DD format. |
| `timezone` | query | `string` | no | Timezone used when filtering by date range. |
