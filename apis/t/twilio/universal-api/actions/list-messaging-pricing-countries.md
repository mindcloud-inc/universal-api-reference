# Twilio: List Messaging Pricing Countries

Retrieves messaging country pricing from Twilio.

```
GET https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-messaging-pricing-countries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Twilio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-messaging-pricing-countries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/twilio/latest/actions/list-messaging-pricing-countries?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "countries": [
        {
          "country": "string",
          "isoCountry": "string",
          "url": "https://example.com"
        }
      ],
      "meta": {
        "firstPageUrl": "https://example.com",
        "key": "string",
        "nextPageUrl": "https://example.com",
        "page": 1,
        "pageSize": 1,
        "previousPageUrl": "https://example.com",
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countries[].country` | string |  |
| `countries[].isoCountry` | string |  |
| `countries[].url` | string |  |
| `meta.firstPageUrl` | string |  |
| `meta.key` | string |  |
| `meta.nextPageUrl` | string |  |
| `meta.page` | number |  |
| `meta.pageSize` | number |  |
| `meta.previousPageUrl` | string |  |
| `meta.url` | string |  |

## Native endpoint

Through the native Twilio API, this operation is `GET https://pricing.twilio.com/v1/Messaging/Countries` (base URL `https://api.twilio.com/2010-04-01`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-messaging-pricing-countries.md) for the provider-specific parameters and requirements.

