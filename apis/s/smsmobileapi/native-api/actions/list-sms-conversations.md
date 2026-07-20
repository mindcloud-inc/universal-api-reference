# List SMS Conversations with Smsmobileapi

Retrieves SMS conversations from Smsmobileapi.

## Endpoint

- **Method:** `GET`
- **Path:** `/conversation/sms/list/`
- **Base URL:** `https://api.smsmobileapi.com`
- **Official documentation:** [List SMS Conversations](https://smsmobileapi.com/doc/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `origineConversation` | query | `list` | yes | Choose whether the conversation list is seeded from received or sent SMS logs. Accepted values: `received`, `sent`. |
| `numero` | query | `string` | no | Filter to one specific phone number. |
| `date_from` | query | `date` | no | Only include conversations and messages from this date forward. |
| `date_to` | query | `date` | no | Only include conversations and messages up to this date. |
| `sort` | query | `list` | no | Sort the conversation list ascending or descending. Accepted values: `ASC`, `DESC`. |
| `limit` | query | `number` | no | Maximum number of conversations to return when a phone number is not provided. |
