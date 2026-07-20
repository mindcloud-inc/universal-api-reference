# Ayrshare: Verify Media URL

Verifies a media URL in Ayrshare.

```
GET https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/verify-media-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/verify-media-url?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/verify-media-url?${params}`, {
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
| `url` | string | yes | HTTPS media URL to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "contentType": "string",
      "height": 1,
      "message": "string",
      "status": "string",
      "urlExists": true,
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Ayrshare error code. |
| `contentType` | string | Detected content type. |
| `height` | number | Image height when returned. |
| `message` | string | Verification or error message. |
| `status` | string | Verification status. |
| `urlExists` | boolean | Whether the media URL exists. |
| `width` | number | Image width when returned. |

## Native endpoint

Through the native Ayrshare API, this operation is `POST /media/urlExists` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-media-url.md) for the provider-specific parameters and requirements.

