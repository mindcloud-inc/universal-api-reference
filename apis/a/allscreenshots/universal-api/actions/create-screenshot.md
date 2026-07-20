# Allscreenshots: Create Screenshot

Creates a new website capture in Allscreenshots.

```
POST https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/create-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Allscreenshots `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/create-screenshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/allscreenshots/latest/actions/create-screenshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The webpage URL to capture. |
| `format` | string | no | Output format such as png, jpeg, webp, or pdf. |
| `full_page` | boolean | no | Capture the full scrollable page instead of the visible viewport. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `response_type` | string | no | How the screenshot result should be returned. |
| `delay` | number | no | Milliseconds to wait before capturing the page. |
| `dark_mode` | boolean | no | Render the page with a dark color scheme when supported. |
| `block_ads` | boolean | no | Block common ad networks during capture. |
| `block_cookie_banners` | boolean | no | Try to hide cookie consent banners during capture. |
| `outputs[]` | array<object> | no | Optional multi-output extraction configuration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cached": true,
      "contentType": "string",
      "data": "string",
      "encoding": "string",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "format": "string",
      "height": 1,
      "renderTimeMs": 1,
      "size": 1,
      "storageUrl": "https://example.com",
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
| `cached` | boolean |  |
| `contentType` | string |  |
| `data` | string |  |
| `encoding` | string |  |
| `expiresAt` | date |  |
| `format` | string |  |
| `height` | number |  |
| `renderTimeMs` | number |  |
| `size` | number |  |
| `storageUrl` | string |  |
| `url` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Allscreenshots API, this operation is `POST /v1/screenshots` (base URL `https://api.allscreenshots.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-screenshot.md) for the provider-specific parameters and requirements.

