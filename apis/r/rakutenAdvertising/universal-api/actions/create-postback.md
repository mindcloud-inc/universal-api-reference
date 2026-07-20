# Rakuten Advertising: Create postback

Creates a new postback in Rakuten Advertising.

```
POST https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/create-postback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/create-postback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "isActive": "true",
  "sid": "4693234",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/create-postback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "isActive": "true",
    "sid": "4693234",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isActive` | boolean | yes | Whether the postback configuration is active. Default: `true`. |
| `sid` | string | yes | Rakuten publisher SID. Default: `4693234`. |
| `url` | string | yes | URL that Rakuten calls for transaction postbacks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "isActive": true,
      "message": "string",
      "publisherId": "string",
      "sid": "string",
      "success": true,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isActive` | boolean |  |
| `message` | string |  |
| `publisherId` | string |  |
| `sid` | string |  |
| `success` | boolean |  |
| `url` | string |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `POST /v1/postback` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-postback.md) for the provider-specific parameters and requirements.

