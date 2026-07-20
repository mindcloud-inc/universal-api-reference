# CometAPI: Kling Image Expansion

Creates an expanded Kling image in CometAPI.

```
POST https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-image-expansion
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-image-expansion" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "string",
  "rightExpansionRatio": 1,
  "upExpansionRatio": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-image-expansion', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image": "string",
    "rightExpansionRatio": 1,
    "upExpansionRatio": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image` | string | yes | Image input. |
| `rightExpansionRatio` | number | yes | Right expansion ratio. |
| `upExpansionRatio` | number | yes | Upper expansion ratio. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        {}
      ],
      "status": "string",
      "task_id": "string"
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
| `task_id` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `POST /kling/v1/images/editing/expand` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/kling-image-expansion.md) for the provider-specific parameters and requirements.

