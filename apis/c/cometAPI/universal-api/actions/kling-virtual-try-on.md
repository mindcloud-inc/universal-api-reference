# CometAPI: Kling Virtual Try On

Creates a Kling virtual try-on image in CometAPI.

```
POST https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-virtual-try-on
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-virtual-try-on" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clothImage": "string",
  "humanImage": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-virtual-try-on', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clothImage": "string",
    "humanImage": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `clothImage` | string | yes | Clothing image. |
| `humanImage` | string | yes | Human image. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
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
| `data` | object |  |
| `status` | string |  |
| `task_id` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `POST /kling/v1/images/kolors-virtual-try-on` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/kling-virtual-try-on.md) for the provider-specific parameters and requirements.

