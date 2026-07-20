# TLY Link Shortener: Create Pixel

Creates a new pixel in TLY Link Shortener.

```
POST https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/create-pixel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TLY Link Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/create-pixel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "pixelId": "string",
  "pixelType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tLYLinkShortener/latest/actions/create-pixel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "pixelId": "string",
    "pixelType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The pixel display name. |
| `pixelId` | string | yes | The provider pixel identifier. |
| `pixelType` | string | yes | The pixel provider type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
      "pixel_id": "string",
      "pixel_type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `id` | number |  |
| `name` | string |  |
| `pixel_id` | string |  |
| `pixel_type` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native TLY Link Shortener API, this operation is `POST /api/v1/link/pixel` (base URL `https://api.t.ly`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pixel.md) for the provider-specific parameters and requirements.

