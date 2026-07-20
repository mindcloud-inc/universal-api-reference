# Deploy Bot Flow with QWIC

Deploys a flow for a QWIC bot.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/bots/:bot_id/deploy`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Deploy Bot Flow](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#deploy-bot-flow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bot_id` | path | `number` | yes | The bot ID. |
| `flow_diagram` | body | `string` | yes | The bot flow JSON string. |
