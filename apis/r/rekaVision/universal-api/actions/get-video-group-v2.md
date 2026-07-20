# Reka Vision: Get Video Group (V2)

Retrieves a video group from Reka Vision.

```
GET https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-video-group-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-video-group-v2?connectionId=$CONNECTION_ID&groupId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/get-video-group-v2?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes |  |

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

Through the native Reka Vision API, this operation is `GET /v2/video-groups/:groupId` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-video-group-v2.md) for the provider-specific parameters and requirements.

