# List Missed Chats By Date Range with Social Intents

Retrieves missed chats from Social Intents using a date range.

## Endpoint

- **Method:** `GET`
- **Path:** `/missedchats`
- **Base URL:** `https://www.socialintents.com/v1/api`
- **Official documentation:** [List Missed Chats By Date Range](https://www.socialintents.com/docs/integrations/rest-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date_from` | query | `string` | yes | Start date for missed-chat filtering. |
| `date_to` | query | `string` | yes | End date for missed-chat filtering. |
