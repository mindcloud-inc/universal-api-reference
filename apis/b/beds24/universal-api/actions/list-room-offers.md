# Beds24: List Room Offers

Retrieves room offers from Beds24 by stay criteria.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-room-offers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-room-offers?connectionId=$CONNECTION_ID&arrival=string&departure=string&numAdults=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "arrival": "string",
  "departure": "string",
  "numAdults": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-room-offers?${params}`, {
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
| `arrival` | string | yes | Offer search arrival date in YYYY-MM-DD format. |
| `departure` | string | yes | Offer search departure date in YYYY-MM-DD format. |
| `numAdults` | number | yes | Number of adults for the offer search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "offers": [
        {}
      ],
      "propertyId": 1,
      "roomId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `offers` | array<object> | Calculated offers returned for the search criteria. |
| `propertyId` | number | Beds24 property ID the offer belongs to. |
| `roomId` | number | Beds24 room ID the offer belongs to. |

## Native endpoint

Through the native Beds24 API, this operation is `GET /inventory/rooms/offers` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-room-offers.md) for the provider-specific parameters and requirements.

