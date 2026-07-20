# 1001fx: HTML to Image

Converts HTML or a URL into an image.

```
POST https://connect.mindcloud.co/v1/universal/fx/latest/actions/html-to-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1001fx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fx/latest/actions/html-to-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "outputFormat": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fx/latest/actions/html-to-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "outputFormat": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fullPage` | boolean | no | Whether to capture the full rendered page. |
| `height` | number | no | Output height in pixels. |
| `html` | string | no | HTML source to render. |
| `outputFormat` | string | yes | Output image format. |
| `replacements[]` | array | no | Replacement values used before rendering the HTML. |
| `url` | string | no | URL to render when not passing raw HTML. |
| `width` | number | no | Output width in pixels. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native 1001fx API returns.

## Native endpoint

Through the native 1001fx API, this operation is `POST /images/html2image` (base URL `https://api.1001fx.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/html-to-image.md) for the provider-specific parameters and requirements.

