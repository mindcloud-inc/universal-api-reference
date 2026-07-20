# SCRNIFY.com: Capture Screenshot or Video

Captures a screenshot or video with SCRNIFY.com.

```
GET https://connect.mindcloud.co/v1/universal/sCRNIFYcom/latest/actions/capture-screenshot-or-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SCRNIFY.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sCRNIFYcom/latest/actions/capture-screenshot-or-video?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&format=0&type=0&width=1280" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "format": "0",
  "type": "0",
  "width": "1280"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sCRNIFYcom/latest/actions/capture-screenshot-or-video?${params}`, {
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
| `url` | string | yes | URL of the page to capture. Example: `https://example.com`. |
| `format` | list | yes | Output format. One of: `0`, `1`, `2`, `3`, `4`. |
| `type` | list | yes | Capture type. One of: `0`, `1`. |
| `width` | number | yes | Viewport width in pixels. Example: `1280`. |
| `height` | number | no | Viewport height in pixels. Example: `720`. |
| `fullPage` | boolean | no | Capture the full page. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SCRNIFY.com API returns.

## Native endpoint

Through the native SCRNIFY.com API, this operation is `GET /capture` (base URL `https://api.scrnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/capture-screenshot-or-video.md) for the provider-specific parameters and requirements.

