# Bookingmood: Search Availability

Finds Bookingmood product availability by interval, occupancy, and attribute options.

```
GET https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/search-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookingmood `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/search-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/search-availability?${params}`, {
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
| `interval.end` | string | no | End date for the availability search interval. |
| `interval.start` | string | no | Start date for the availability search interval. |
| `occupancy` | string | no | Occupancy per capacity group. |
| `optionIds` | string | no | Attribute option IDs to filter search results. |
| `showBookedAs` | string | no | How to interpret booked events. |
| `showClosedAs` | string | no | How to interpret closed events. |
| `showPendingAs` | string | no | How to interpret pending events. Default: `TENTATIVE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availability": "string",
      "match": true,
      "occupancyMatches": true,
      "optionsMatch": true,
      "price": {},
      "product": {},
      "productId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availability` | string |  |
| `match` | boolean |  |
| `occupancyMatches` | boolean |  |
| `optionsMatch` | boolean |  |
| `price` | object |  |
| `product` | object |  |
| `productId` | string |  |

## Native endpoint

Through the native Bookingmood API, this operation is `POST /search` (base URL `https://api.bookingmood.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-availability.md) for the provider-specific parameters and requirements.

