# Stack AI: Run Action



```
POST https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/run-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stack AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/run-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionId": "string",
  "providerId": "string",
  "projectId": "string",
  "inputs": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/stackAI/latest/actions/run-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionId": "string",
    "providerId": "string",
    "projectId": "string",
    "inputs": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actionId` | string | yes | The action identifier. |
| `providerId` | string | yes | The provider identifier. |
| `projectId` | string | yes | The project identifier. |
| `inputs` | object | yes | The action inputs object. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Stack AI API returns.

## Native endpoint

Through the native Stack AI API, this operation is `POST /tools/stackai/providers/:provider_id/actions/:action_id/run` (base URL `https://api.stack-ai.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-action.md) for the provider-specific parameters and requirements.

