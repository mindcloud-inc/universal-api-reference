# Create Bot with QWIC

Creates a new bot in QWIC.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/bot`
- **Base URL:** `https://app.qwic.ai`
- **Official documentation:** [Create Bot](https://qwic-1.gitbook.io/help/building-agents/integrations/public-apis#create-a-bot)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The bot name. |
| `template_id` | body | `number` | yes | The reference bot template ID. |
