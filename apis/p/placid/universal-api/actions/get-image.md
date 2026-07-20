# Placid: Get Image

Retrieves an image render from Placid.

```
GET https://connect.mindcloud.co/v1/universal/placid/latest/actions/get-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/placid/latest/actions/get-image?connectionId=$CONNECTION_ID&imageId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/placid/latest/actions/get-image?${params}`, {
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
| `imageId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "id": 1,
      "imageUrl": "https://example.com",
      "passthrough": "string",
      "pollingUrl": "https://example.com",
      "status": "string",
      "transferUrl": "https://example.com",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> |  |
| `id` | number |  |
| `imageUrl` | string |  |
| `passthrough` | string |  |
| `pollingUrl` | string |  |
| `status` | string |  |
| `transferUrl` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Placid API, this operation is `GET /api/rest/images/:imageId` (base URL `https://api.placid.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image.md) for the provider-specific parameters and requirements.

