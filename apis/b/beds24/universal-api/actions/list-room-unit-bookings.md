# Beds24: List Room Unit Bookings

Retrieves unit booking dates from Beds24.

```
GET https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-room-unit-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beds24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-room-unit-bookings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beds24/latest/actions/list-room-unit-bookings?${params}`, {
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
      "name": "Ava Chen",
      "propertyId": 1,
      "qty": 1,
      "roomId": 1,
      "unitBookings": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string |  |
| `propertyId` | number |  |
| `qty` | number |  |
| `roomId` | number |  |
| `unitBookings` | object |  |

## Native endpoint

Through the native Beds24 API, this operation is `GET /inventory/rooms/unitBookings` (base URL `https://beds24.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-room-unit-bookings.md) for the provider-specific parameters and requirements.

