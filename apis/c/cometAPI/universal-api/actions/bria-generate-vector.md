# CometAPI: Bria Generate Vector

Creates Bria vector graphics in CometAPI.

```
POST https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/bria-generate-vector
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/bria-generate-vector" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "guidanceMethod2Scale": 1,
  "prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/bria-generate-vector', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "guidanceMethod2Scale": 1,
    "prompt": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `guidanceMethod2Scale` | number | yes | Required Bria guidance scale. |
| `prompt` | string | yes | Text prompt for vector generation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | array<object> |  |
| `status` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `POST /bria/text-to-vector` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bria-generate-vector.md) for the provider-specific parameters and requirements.

