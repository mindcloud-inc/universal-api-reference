# JmpTo: Create Pixel

Creates a pixel in JmpTo.

```
POST https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/create-pixel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JmpTo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/create-pixel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "string",
  "name": "Ava Chen",
  "tag": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jmpTo/latest/actions/create-pixel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "string",
    "name": "Ava Chen",
    "tag": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | string | yes | Pixel type such as gtmpixel, gapixel, fbpixel, adwordspixel, linkedinpixel, twitterpixel, adrollpixel, quorapixel, pinterest, bing, snapchat, reddit, or tiktok. |
| `name` | string | yes | Custom name for the pixel. |
| `tag` | string | yes | The tag for the pixel. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": 1,
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | number | Provider success/error code. |
| `id` | string | Pixel ID returned by the provider. |

## Native endpoint

Through the native JmpTo API, this operation is `POST /pixel/add` (base URL `https://jmpto.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pixel.md) for the provider-specific parameters and requirements.

