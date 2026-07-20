# SCRNIFY.com: Capture Selector MP4 Video

Captures an MP4 video of a selected element with SCRNIFY.com.

```
GET https://connect.mindcloud.co/v1/universal/sCRNIFYcom/latest/actions/capture-selector-mp4-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SCRNIFY.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sCRNIFYcom/latest/actions/capture-selector-mp4-video?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&selector=body" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "selector": "body"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sCRNIFYcom/latest/actions/capture-selector-mp4-video?${params}`, {
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
| `selector` | string | yes | CSS selector of the element to capture. Example: `body`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SCRNIFY.com API returns.

## Native endpoint

Through the native SCRNIFY.com API, this operation is `GET /capture` (base URL `https://api.scrnify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/capture-selector-mp4-video.md) for the provider-specific parameters and requirements.

