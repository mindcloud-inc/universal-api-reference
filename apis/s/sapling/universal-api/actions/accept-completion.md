# Sapling: Accept Completion

Records an accepted autocomplete completion in Sapling.

```
PUT https://connect.mindcloud.co/v1/universal/sapling/latest/actions/accept-completion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sapling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sapling/latest/actions/accept-completion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "completionId": "string",
  "query": "string",
  "completion": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sapling/latest/actions/accept-completion', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "completionId": "string",
    "query": "string",
    "completion": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `completionId` | string | yes | Completion UUID returned from autocomplete. |
| `query` | string | yes | The original query used to generate the completion. |
| `completion` | string | yes | The accepted completion string. |
| `sessionId` | string | no | Document or session identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |

## Native endpoint

Through the native Sapling API, this operation is `POST /api/v1/complete/:completionId/accept` (base URL `https://api.sapling.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/accept-completion.md) for the provider-specific parameters and requirements.

