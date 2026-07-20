# ScreenshotOne: Take Screenshot



```
GET https://connect.mindcloud.co/v1/universal/screenshotOne/latest/actions/take-screenshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScreenshotOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenshotOne/latest/actions/take-screenshot?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/screenshotOne/latest/actions/take-screenshot?${params}`, {
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
        "imageSize": {
          "height": "string",
          "width": "string"
        },
        "pageTitle": "string"
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
| `metadata.imageSize.height` | string |  |
| `metadata.imageSize.width` | string |  |
| `metadata.pageTitle` | string |  |
| `screenshotUrl` | string |  |

## Native endpoint

Through the native ScreenshotOne API, this operation is `GET /take` (base URL `https://api.screenshotone.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/take-screenshot.md) for the provider-specific parameters and requirements.

