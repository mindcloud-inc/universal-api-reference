# Routee: URL shortener

Creates a shortened URL in Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/url-shortener
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/url-shortener" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "longUrl": "https://example.com",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/url-shortener', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "longUrl": "https://example.com",
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | A human readable name for the shortened url. This will help identify the url in a table, or when fetching analytics data. |
| `longUrl` | string | yes | The url to be shortened. |
| `domain` | string | yes | The domain to use when shortening the url. Will be one of the domains registered by the customer, if one is not available we will return an error. |
| `validity` | number | no | [Optional] For Premium and Enterprise packages the max will be set to 5.184e+6 and 7.776e+6 respectively. |
| `callbackUrl` | string | no | [Optional] The callback we call when a link is clicked. Payload information can be found [here](/docs/callback-url-webhook-1). |
| `tags` | object | no | [Optional] A map of string field values to store information |

## Response

```json
{
  "success": true,
  "data": [
    {
      "shortenUrls": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shortenUrls[]` | array<object> |  |
| `shortenUrls[].callbackUrl` | string |  |
| `shortenUrls[].createdAt` | string |  |
| `shortenUrls[].expirationDate` | string |  |
| `shortenUrls[].link` | string |  |
| `shortenUrls[].longUrl` | string |  |
| `shortenUrls[].name` | string |  |
| `shortenUrls[].tags` | object |  |
| `shortenUrls[].tags.tag1` | string |  |
| `shortenUrls[].tags.tag2` | string |  |
| `shortenUrls[].trackingId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /shorten/urls` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/url-shortener.md) for the provider-specific parameters and requirements.

