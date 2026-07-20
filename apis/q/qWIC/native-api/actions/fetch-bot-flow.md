# Fetch Bot Flow with QWIC

Retrieves the flow for a QWIC bot.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/bots/:bot_id/flow`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Fetch Bot Flow](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#fetch-bot-flow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | path | `number` | yes | The bot ID. |
