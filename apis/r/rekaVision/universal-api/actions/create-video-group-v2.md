# Reka Vision: Create Video Group (V2)

Creates a new video group in Reka Vision.

```
POST https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/create-video-group-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/create-video-group-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/create-video-group-v2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "groupId": "string",
      "metadata": {},
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `groupId` | string |  |
| `metadata` | object |  |
| `name` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Reka Vision API, this operation is `POST /v2/video-groups` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video-group-v2.md) for the provider-specific parameters and requirements.

