# PixelBin.io: Get Transformation Context

Retrieves transformation context from a PixelBin.io URL.

```
GET https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-transformation-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PixelBin.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-transformation-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pixelBinio/latest/actions/get-transformation-context?${params}`, {
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
| `url` | string | no | PixelBin CDN URL with transformation steps applied. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "context": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `context` | object | Parsed transformation context returned by PixelBin for the supplied transformed CDN URL. |

## Native endpoint

Through the native PixelBin.io API, this operation is `GET /service/platform/transformation/context` (base URL `https://api.pixelbin.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-transformation-context.md) for the provider-specific parameters and requirements.

