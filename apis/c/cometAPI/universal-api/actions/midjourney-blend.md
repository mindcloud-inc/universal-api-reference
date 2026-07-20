# CometAPI: Midjourney Blend

Creates a Midjourney blend task in CometAPI.

```
POST https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/midjourney-blend
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/midjourney-blend" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "base64Array[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/midjourney-blend', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "base64Array[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `base64Array[]` | array<string> | yes | Base64 image array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "description": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `description` | string |  |
| `result` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `POST /mj/submit/blend` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/midjourney-blend.md) for the provider-specific parameters and requirements.

