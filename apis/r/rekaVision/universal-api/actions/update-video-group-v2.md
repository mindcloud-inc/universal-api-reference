# Reka Vision: Update Video Group (V2)

Updates an existing video group in Reka Vision.

```
PUT https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/update-video-group-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/update-video-group-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/update-video-group-v2', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes |  |
| `name` | string | no |  |

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

Through the native Reka Vision API, this operation is `PATCH /v2/video-groups/:groupId` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-video-group-v2.md) for the provider-specific parameters and requirements.

