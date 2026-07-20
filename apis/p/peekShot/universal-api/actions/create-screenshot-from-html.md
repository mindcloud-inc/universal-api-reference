# PeekShot: Create Screenshot from HTML

Creates a screenshot from HTML in PeekShot.

```
POST https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/create-screenshot-from-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PeekShot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/create-screenshot-from-html" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/peekShot/latest/actions/create-screenshot-from-html', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "html": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Unique project identifier. |
| `html` | string | yes | HTML content to capture. |
| `width` | string | no | Screenshot width. Docs default: 1280. |
| `height` | string | no | Screenshot height. Docs default: 1024. |
| `fileType` | string | no | Output format: jpeg, png, webp, or avif. |
| `delay` | string | no | Time in seconds to wait before capturing. |
| `fullPage` | string | no | Capture the full page instead of only the viewport. |
| `emulateDevice` | string | no | Render the HTML using a supported device profile. |
| `retina` | string | no | Use true for higher-resolution screenshots. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "creditRequired": 1,
        "organizationId": 1,
        "requestId": 1
      },
      "message": "string",
      "status": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.creditRequired` | number | Credits required for the request. |
| `data.organizationId` | number | Organization ID returned by PeekShot. |
| `data.requestId` | number | Created screenshot request ID. |
| `message` | string | Provider message. |
| `status` | string | Request status. |
| `statusCode` | number | HTTP-style status code returned by the provider. |

## Native endpoint

Through the native PeekShot API, this operation is `POST /html-to-image` (base URL `https://api.peekshot.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-screenshot-from-html.md) for the provider-specific parameters and requirements.

