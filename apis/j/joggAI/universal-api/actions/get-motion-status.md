# JoggAI: Get Motion Status



```
GET https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/get-motion-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/get-motion-status?connectionId=$CONNECTION_ID&motionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "motionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/get-motion-status?${params}`, {
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
| `motionId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatarId": 1,
      "errorMsg": "string",
      "motionId": "string",
      "motionPreviewUrl": "https://example.com",
      "name": "Ava Chen",
      "status": "string",
      "voiceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatarId` | number | Animated avatar ID |
| `errorMsg` | string | Provider error message |
| `motionId` | string | Motion request ID |
| `motionPreviewUrl` | string | Motion preview URL |
| `name` | string | Avatar name |
| `status` | string | Motion status |
| `voiceId` | string | Voice ID |

## Native endpoint

Through the native JoggAI API, this operation is `GET /v2/photo_avatar` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-motion-status.md) for the provider-specific parameters and requirements.

