# Storyblok: Get Signed Asset URL

Retrieves a signed URL for a private Storyblok asset.

```
GET https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-signed-asset-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyblok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-signed-asset-url?connectionId=$CONNECTION_ID&filename=https%3A%2F%2Fa.storyblok.com%2Ff%2F88751%2F600x400%2Fsample.png" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filename": "https://a.storyblok.com/f/88751/600x400/sample.png"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyblok/latest/actions/get-signed-asset-url?${params}`, {
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
| `filename` | string | yes | The Storyblok asset URL to sign. Default: `https://a.storyblok.com/f/88751/600x400/sample.png`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "asset": {
        "filename": "Ava Chen",
        "signed_url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `asset` | object | The asset response. |
| `asset.filename` | string | The requested asset filename. |
| `asset.signed_url` | string | The signed asset URL. |

## Native endpoint

Through the native Storyblok API, this operation is `GET /assets/me` (base URL `https://api.storyblok.com/v2/cdn`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-signed-asset-url.md) for the provider-specific parameters and requirements.

