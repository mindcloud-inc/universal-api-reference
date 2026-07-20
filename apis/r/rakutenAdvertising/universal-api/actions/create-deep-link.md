# Rakuten Advertising: Create deep link

Creates a deep link in Rakuten Advertising.

```
POST https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/create-deep-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rakuten Advertising `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/create-deep-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "advertiserId": 1,
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rakutenAdvertising/latest/actions/create-deep-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "advertiserId": 1,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `advertiserId` | number | yes | Rakuten advertiser ID for the deep link. |
| `url` | string | yes | Destination URL to turn into a Rakuten deep link. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "advertiserId": "string",
      "deepLinkUrl": "https://example.com",
      "message": "string",
      "success": true,
      "u1": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `advertiserId` | string |  |
| `deepLinkUrl` | string |  |
| `message` | string |  |
| `success` | boolean |  |
| `u1` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Rakuten Advertising API, this operation is `POST /v1/links/deep_links` (base URL `https://api.linksynergy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-deep-link.md) for the provider-specific parameters and requirements.

