# Valyu: Create DeepResearch Task



```
POST https://connect.mindcloud.co/v1/universal/valyu/latest/actions/create-deep-research-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Valyu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/valyu/latest/actions/create-deep-research-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/valyu/latest/actions/create-deep-research-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mode` | string | no | Research mode controlling depth and cost. |
| `query` | string | yes | The research query or question. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deepresearchId": "string",
      "metadata": {},
      "mode": "string",
      "public": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `deepresearchId` | string |  |
| `metadata` | object |  |
| `mode` | string |  |
| `public` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Valyu API, this operation is `POST /deepresearch/tasks` (base URL `https://api.valyu.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deep-research-task.md) for the provider-specific parameters and requirements.

