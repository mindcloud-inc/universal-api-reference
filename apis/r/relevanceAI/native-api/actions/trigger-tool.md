# Trigger Tool with Relevance AI

## Endpoint

- **Method:** `POST`
- **Path:** `/studios/:toolId/trigger_limited`
- **Base URL:** `https://api-{region}.stack.tryrelevance.com/latest`
- **Official documentation:** [Trigger Tool](https://sdk.relevanceai.com/concepts/10_1/tools)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project` | body | `string` | yes | The Relevance AI project ID. Use the same project value as your connection. |
| `toolId` | path | `string` | yes | The Relevance AI tool id to run. |
| `params` | body | `object` | no | Optional params object to pass into the tool run. |
