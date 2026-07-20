# JoggAI: Get Photo Avatar Status



```
GET https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/get-photo-avatar-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/get-photo-avatar-status?connectionId=$CONNECTION_ID&photoId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "photoId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/get-photo-avatar-status?${params}`, {
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
| `photoId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageKeyList": [
        [
          "string"
        ]
      ],
      "imageUrlList": [
        [
          "https://example.com"
        ]
      ],
      "msg": "string",
      "photoId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imageKeyList[]` | array<string> | Generated image keys |
| `imageUrlList[]` | array<string> | Generated image URLs |
| `msg` | string | Provider status message |
| `photoId` | string | Photo avatar request ID |
| `status` | string | Generation status |

## Native endpoint

Through the native JoggAI API, this operation is `GET /v2/photo_avatar/photo` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-photo-avatar-status.md) for the provider-specific parameters and requirements.

