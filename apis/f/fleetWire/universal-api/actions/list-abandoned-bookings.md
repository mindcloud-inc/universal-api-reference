# FleetWire: List Abandoned Bookings

Retrieves abandoned bookings from FleetWire.

```
GET https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/list-abandoned-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FleetWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/list-abandoned-bookings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/list-abandoned-bookings?${params}`, {
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
      "booking": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `booking` | array<object> | Abandoned booking rows returned by FleetWire. |

## Native endpoint

Through the native FleetWire API, this operation is `GET /api/v2/zapier/abandoned-bookings` (base URL `https://api.fleetwire.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-abandoned-bookings.md) for the provider-specific parameters and requirements.

