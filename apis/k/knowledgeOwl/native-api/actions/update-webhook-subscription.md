# Update Webhook Subscription with KnowledgeOwl

## Endpoint

- **Method:** `PUT`
- **Path:** `/webhook/:id.json`
- **Base URL:** `https://app.knowledgeowl.com/api/head`
- **Official documentation:** [Update Webhook Subscription](https://support.knowledgeowl.com/help/api-endpoint-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | — |
| `endpoint` | body | `string` | yes | — |
| `event` | body | `list<string>` | yes | Send multiple values as a array. |
