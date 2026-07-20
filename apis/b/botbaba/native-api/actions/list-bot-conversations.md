# List Bot Conversations with Botbaba

## Endpoint

- **Method:** `GET`
- **Path:** `/api/GetBotConversations`
- **Base URL:** `https://app.botbaba.io`
- **Official documentation:** [List Bot Conversations](https://app.botbaba.io/swagger/ui/index)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | query | `number` | yes | The Botbaba bot identifier. |
| `page` | query | `number` | no | Optional result page number. |
| `pageSize` | query | `number` | no | Optional page size. |
