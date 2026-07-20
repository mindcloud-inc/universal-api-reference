# Unregister Webhook with GoZen DeepAgent

Unregisters a webhook in GoZen DeepAgent.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/integration/zapierapp/webhook`
- **Base URL:** `https://api.deepbot.gozen.io`
- **Official documentation:** [Unregister Webhook](https://docs.gozen.io/deepagent/api-docs/zapier/unregister-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `knowledgebaseId` | body | `string` | yes | Chatbot ID. |
| `integrationId` | body | `string` | yes | Integration ID in GoZen's database. |
