# Geral: Get Pixel

Retrieves a pixel from Geral by ID.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-pixel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-pixel?connectionId=$CONNECTION_ID&pixelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pixelId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-pixel?${params}`, {
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
| `pixelId` | number | yes | The pixel ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datetime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "last_datetime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "pixel": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datetime` | date | Creation timestamp. |
| `id` | number | Pixel ID. |
| `last_datetime` | date | Last update timestamp. |
| `name` | string | Pixel name. |
| `pixel` | string | Pixel identifier. |
| `type` | string | Pixel provider type. |

## Native endpoint

Through the native Geral API, this operation is `GET /pixels/:pixel_id` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-pixel.md) for the provider-specific parameters and requirements.

