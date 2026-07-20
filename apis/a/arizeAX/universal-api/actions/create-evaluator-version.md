# Arize AX: Create Evaluator Version

Creates a new evaluator version in Arize AX.

```
POST https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/create-evaluator-version
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Arize AX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/create-evaluator-version" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "commitMessage": "string",
  "evaluatorId": "string",
  "templateConfig": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/arizeAX/latest/actions/create-evaluator-version', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "commitMessage": "string",
    "evaluatorId": "string",
    "templateConfig": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commitMessage` | string | yes |  |
| `evaluatorId` | string | yes |  |
| `templateConfig` | object | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Arize AX API returns.

## Native endpoint

Through the native Arize AX API, this operation is `POST /v2/evaluators/{evaluator_id}/versions` (base URL `https://api.arize.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-evaluator-version.md) for the provider-specific parameters and requirements.

