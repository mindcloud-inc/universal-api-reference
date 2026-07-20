# Recut URL Shortener: Create Pixel

Creates a tracking pixel in Recut URL Shortener.

```
POST https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/create-pixel
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recut URL Shortener `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/create-pixel" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "type": "gtmpixel",
  "name": "MindCloud Pixel",
  "tag": "GTM-MINDCLD"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recutURLShortener/latest/actions/create-pixel', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "type": "gtmpixel",
    "name": "MindCloud Pixel",
    "tag": "GTM-MINDCLD"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `type` | list | yes | gtmpixel \| gapixel \| fbpixel \| adwordspixel \| linkedinpixel \| twitterpixel \| adrollpixel \| quorapixel \| pinterest \| bing \| snapchat \| reddit \| tiktok One of: `0`, `1`, `10`, `11`, `12`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. Example: `gtmpixel`. |
| `name` | string | yes | Custom name for your pixel Example: `MindCloud Pixel`. |
| `tag` | string | yes | The tag for the pixel Example: `GTM-MINDCLD`. |

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
| `error` | number |  |
| `id` | string |  |

## Native endpoint

Through the native Recut URL Shortener API, this operation is `POST /pixel/add` (base URL `https://app.recut.in/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-pixel.md) for the provider-specific parameters and requirements.

