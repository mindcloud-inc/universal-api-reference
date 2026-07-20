# Get Conversation Detail with AssignX

Retrieves detailed conversation data from AssignX.

## Endpoint

- **Method:** `GET`
- **Path:** `agents/:id/conversations/:cid`
- **Base URL:** `https://api.agentx.so/api/v1/access/`
- **Official documentation:** [Get Conversation Detail](https://docs.agentx.so/reference/get_api-v1-access-agents-id-conversations-cid-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The AssignX agent identifier. |
| `cid` | path | `string` | yes | The AssignX conversation identifier. |
