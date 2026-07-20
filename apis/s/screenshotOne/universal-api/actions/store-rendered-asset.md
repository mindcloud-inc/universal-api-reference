# ScreenshotOne: Store Rendered Asset



```
GET https://connect.mindcloud.co/v1/universal/screenshotOne/latest/actions/store-rendered-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ScreenshotOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenshotOne/latest/actions/store-rendered-asset?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com&storagePath=latest%2Fexample" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com",
  "storagePath": "latest/example"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/screenshotOne/latest/actions/store-rendered-asset?${params}`, {
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
| `storagePath` | string | yes | Example: `latest/example`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "screenshotUrl": "https://example.com",
      "store": {
        "location": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `screenshotUrl` | string |  |
| `store.location` | string |  |

## Native endpoint

Through the native ScreenshotOne API, this operation is `GET /take` (base URL `https://api.screenshotone.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/store-rendered-asset.md) for the provider-specific parameters and requirements.

