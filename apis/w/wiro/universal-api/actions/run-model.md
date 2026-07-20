# Wiro: Run Model

Starts an AI model run in Wiro and returns a task ID.

```
POST https://connect.mindcloud.co/v1/universal/wiro/latest/actions/run-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wiro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wiro/latest/actions/run-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wiro/latest/actions/run-model', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        "string"
      ],
      "result": true,
      "socketaccesstoken": "string",
      "taskid": "string",
      "tasklist": [
        {}
      ],
      "tasktoken": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<string> |  |
| `result` | boolean |  |
| `socketaccesstoken` | string |  |
| `taskid` | string |  |
| `tasklist` | array<object> |  |
| `tasktoken` | string |  |

## Native endpoint

Through the native Wiro API, this operation is `POST /Run/{slugowner}/{slugproject}` (base URL `https://api.wiro.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/run-model.md) for the provider-specific parameters and requirements.

