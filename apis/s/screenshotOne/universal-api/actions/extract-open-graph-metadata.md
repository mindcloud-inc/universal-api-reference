# ScreenshotOne: Extract Open Graph Metadata



```
GET https://connect.mindcloud.co/v1/universal/screenshotOne/latest/actions/extract-open-graph-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScreenshotOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenshotOne/latest/actions/extract-open-graph-metadata?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/screenshotOne/latest/actions/extract-open-graph-metadata?${params}`, {
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
| `url` | string | yes | Example: `https://example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cacheUrl": "https://example.com",
      "metadata": {
        "openGraph": {
          "description": "string",
          "image": "string",
          "title": "string"
        }
      },
      "screenshotUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cacheUrl` | string |  |
| `metadata.openGraph.description` | string |  |
| `metadata.openGraph.image` | string |  |
| `metadata.openGraph.title` | string |  |
| `screenshotUrl` | string |  |

## Native endpoint

Through the native ScreenshotOne API, this operation is `GET /take` (base URL `https://api.screenshotone.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-open-graph-metadata.md) for the provider-specific parameters and requirements.

