# Picsart: Upscale Image

Creates an upscaled image in Picsart.

```
POST https://connect.mindcloud.co/v1/universal/picsart/latest/actions/upscale-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Picsart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/picsart/latest/actions/upscale-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageUrl": "https://pastatic.picsart.com/31399405932227146498.png",
  "upscaleFactor": "2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/picsart/latest/actions/upscale-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageUrl": "https://pastatic.picsart.com/31399405932227146498.png",
    "upscaleFactor": "2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageUrl` | string | yes | Source image URL. Example: `https://pastatic.picsart.com/31399405932227146498.png`. |
| `upscaleFactor` | number | yes | Choose one of the supported upscale factors. Example: `2`. |
| `format` | string | no | Optional output image format. Example: `JPG`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": "string",
        "url": "https://example.com"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | string |  |
| `data.url` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Picsart API, this operation is `POST /tools/1.0/upscale` (base URL `https://api.picsart.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upscale-image.md) for the provider-specific parameters and requirements.

