# Register Webhook with GoZen DeepAgent

Registers a webhook in GoZen DeepAgent.

## Endpoint

- **Method:** `POST`
- **Path:** `/integration/zapierapp/webhook`
- **Base URL:** `https://api.deepbot.gozen.io`
- **Official documentation:** [Register Webhook](https://docs.gozen.io/deepagent/api-docs/zapier/register-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | Webhook URL to receive lead collection events. |
| `knowledgebaseId` | body | `string` | yes | Chat bot ID. |
