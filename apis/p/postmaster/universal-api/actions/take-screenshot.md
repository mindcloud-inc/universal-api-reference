# Postmaster+: Take Screenshot

Takes a screenshot with the Postmaster+ API.

```
POST https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/take-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmaster+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/take-screenshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/take-screenshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deviceScale` | number | no | Device scale factor from 1 to 3. |
| `format` | string | no | Image format: png, jpeg, or webp. One of: `0`, `1`, `2`. |
| `height` | number | no | Viewport height in pixels, between 240 and 1080. |
| `html` | string | no | HTML content to screenshot. Required if url is not provided. |
| `url` | string | no | URL to screenshot. Required if html is not provided. |
| `width` | number | no | Viewport width in pixels, between 320 and 1920. |

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

Through the native Postmaster+ API, this operation is `POST /api/v1/screenshot/take` (base URL `https://postmasterplus.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/take-screenshot.md) for the provider-specific parameters and requirements.

