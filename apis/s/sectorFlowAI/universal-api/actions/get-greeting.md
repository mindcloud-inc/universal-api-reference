# SectorFlow.AI: Get Greeting



```
GET https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/get-greeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SectorFlow.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/get-greeting?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/get-greeting?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | The workspace UUID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SectorFlow.AI API returns.

## Native endpoint

Through the native SectorFlow.AI API, this operation is `GET /chat/{workspaceId}/greeting` (base URL `https://platform.sectorflow.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-greeting.md) for the provider-specific parameters and requirements.

