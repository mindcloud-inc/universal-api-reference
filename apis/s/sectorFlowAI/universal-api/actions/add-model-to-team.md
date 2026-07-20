# SectorFlow.AI: Add Model To Team



```
PUT https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/add-model-to-team
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SectorFlow.AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/add-model-to-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "model": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sectorFlowAI/latest/actions/add-model-to-team', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "model": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `model` | object | yes | The model to add to the team. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SectorFlow.AI API returns.

## Native endpoint

Through the native SectorFlow.AI API, this operation is `POST /models/add-to-team` (base URL `https://platform.sectorflow.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-model-to-team.md) for the provider-specific parameters and requirements.

