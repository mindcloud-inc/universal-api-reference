# List Chat Messages with Framework360

## Endpoint

- **Method:** `GET`
- **Path:** `chat/messages`
- **Base URL:** `https://mindcloudstage0.framework360.site/m/api`
- **Official documentation:** [List Chat Messages](https://mindcloudstage0.myframework360.com/modules/integrazione/developer/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conversation` | query | `number` | yes | Conversation ID to fetch messages for. |
| `page` | query | `number` | no | Results page number. |
| `limit` | query | `number` | no | Maximum number of messages per page. |
| `query` | query | `string` | no | Free-text search term. |
