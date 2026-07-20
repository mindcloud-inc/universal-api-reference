# Giftbit: List Brands

Lists available reward brands in Giftbit.

```
GET https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/list-brands
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giftbit `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/list-brands?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/list-brands?${params}`, {
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
| `region` | number | no |  |
| `search` | string | no |  |
| `currencyIsoCode` | string | no |  |
| `embeddable` | boolean | no |  |
| `minPriceInCents` | number | no |  |
| `maxPriceInCents` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "brands": [
        {}
      ],
      "info": {},
      "limit": 1,
      "number_of_results": 1,
      "offset": 1,
      "total_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `brands` | array<object> |  |
| `info` | object |  |
| `limit` | number |  |
| `number_of_results` | number |  |
| `offset` | number |  |
| `total_count` | number |  |

## Native endpoint

Through the native Giftbit API, this operation is `GET /brands` (base URL `https://api-testbed.giftbit.com/papi/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-brands.md) for the provider-specific parameters and requirements.

