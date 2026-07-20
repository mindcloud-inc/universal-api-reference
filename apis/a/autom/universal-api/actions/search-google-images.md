# Autom: Search Google Images

Finds Google image results in Autom.

```
GET https://connect.mindcloud.co/v1/universal/autom/latest/actions/search-google-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/autom/latest/actions/search-google-images?connectionId=$CONNECTION_ID&query=MindCloud" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "MindCloud"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/autom/latest/actions/search-google-images?${params}`, {
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
| `query` | string | yes | The image search query to run. Example: `MindCloud`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `gl` | string | no | Two-letter Google country code such as us, uk, or fr. Example: `us`. |
| `hl` | string | no | Two-letter Google language code such as en, es, or fr. Example: `en`. |
| `page` | number | no | Result page number to request. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "images": [
        {}
      ],
      "searchParameters": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `images` | array<object> | Structured Google image results. |
| `searchParameters` | object | Resolved search parameters returned by the image request. |

## Native endpoint

Through the native Autom API, this operation is `GET /v1/google/images` (base URL `https://api.autom.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-google-images.md) for the provider-specific parameters and requirements.

