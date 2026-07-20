# Create Webhook Subscription with KnowledgeOwl

## Endpoint

- **Method:** `POST`
- **Path:** `/webhook.json`
- **Base URL:** `https://app.knowledgeowl.com/api/head`
- **Official documentation:** [Create Webhook Subscription](https://support.knowledgeowl.com/help/api-endpoint-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endpoint` | body | `string` | yes | — |
| `event` | body | `list<string>` | yes | Send multiple values as a array. |
