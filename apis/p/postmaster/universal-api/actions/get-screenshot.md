# Postmaster+: Get Screenshot

Retrieves a screenshot from the Postmaster+ API.

```
GET https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/get-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmaster+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/get-screenshot?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/get-screenshot?${params}`, {
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
| `id` | string | yes | The ULID of the screenshot. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "string",
      "createdAt": "string",
      "creditsUsed": 1,
      "deviceScale": 1,
      "format": "string",
      "height": 1,
      "id": "string",
      "message": "string",
      "startedAt": "string",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | string | Completion timestamp. |
| `createdAt` | string | Creation timestamp. |
| `creditsUsed` | number | Credits consumed. |
| `deviceScale` | number | Device scale factor. |
| `format` | string | Image format. |
| `height` | number | Screenshot height. |
| `id` | string | Screenshot ULID. |
| `message` | string | Provider message. |
| `startedAt` | string | Start timestamp. |
| `url` | string | Screenshot URL. |
| `width` | number | Screenshot width. |

## Native endpoint

Through the native Postmaster+ API, this operation is `GET /api/v1/screenshot/:id` (base URL `https://postmasterplus.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-screenshot.md) for the provider-specific parameters and requirements.

