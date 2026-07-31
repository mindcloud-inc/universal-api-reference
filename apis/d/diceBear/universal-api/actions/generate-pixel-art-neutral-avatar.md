# DiceBear: Generate Pixel Art Neutral Avatar



```
GET https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/generate-pixel-art-neutral-avatar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DiceBear `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/generate-pixel-art-neutral-avatar?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/diceBear/latest/actions/generate-pixel-art-neutral-avatar?${params}`, {
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
| `seed` | string | no | Seed value used to generate a deterministic avatar. |

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
| `data` | array<number> | Byte array containing the generated SVG payload. |
| `type` | string | Buffer wrapper type returned by the MindCloud runner for binary-safe SVG output. |

## Native endpoint

Through the native DiceBear API, this operation is `GET /pixel-art-neutral/svg` (base URL `https://api.dicebear.com/10.x`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-pixel-art-neutral-avatar.md) for the provider-specific parameters and requirements.

