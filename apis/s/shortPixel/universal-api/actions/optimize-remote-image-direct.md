# ShortPixel: Optimize Remote Image Direct

Creates an optimized image directly from a remote URL in ShortPixel.

```
POST https://connect.mindcloud.co/v1/universal/shortPixel/latest/actions/optimize-remote-image-direct
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShortPixel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shortPixel/latest/actions/optimize-remote-image-direct" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shortPixel/latest/actions/optimize-remote-image-direct', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | yes | The publicly reachable image URL to optimize and return directly. |
| `lossy` | number | no | 0 for lossless, 1 for lossy, 2 for glossy compression. |
| `wait` | number | no | Maximum seconds to wait for optimization before returning. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Byte array for the optimized image returned directly by ShortPixel. |
| `type` | string | Runtime wrapper type for the raw synchronized reducer output. |

## Native endpoint

Through the native ShortPixel API, this operation is `POST /v2/reducer-sync.php` (base URL `https://api.shortpixel.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/optimize-remote-image-direct.md) for the provider-specific parameters and requirements.

