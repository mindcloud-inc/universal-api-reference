# Get Leads with Chatnode

## Endpoint

- **Method:** `POST`
- **Path:** `get-conversation-ids/:botId`
- **Base URL:** `https://api.public.chatnode.ai/v1`
- **Official documentation:** [Get Leads](https://www.chatnode.ai/docs/developer-guides/api/get-leads)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `botId` | path | `string` | yes | The Chatnode agent id associated with the trained agent model. |
