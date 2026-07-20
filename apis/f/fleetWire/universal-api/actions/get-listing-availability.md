# FleetWire: Get Listing Availability

Retrieves listing availability from FleetWire.

```
GET https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-listing-availability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FleetWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-listing-availability?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-listing-availability?${params}`, {
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
| `end` | string | no | End datetime for the availability check. |
| `listingId` | string | no | Optional FleetWire listing identifier to scope availability. |
| `start` | string | no | Start datetime for the availability check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "listings": [
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
| `listings` | array<object> | Listings annotated with availability information for the requested time range. |

## Native endpoint

Through the native FleetWire API, this operation is `GET /api/v2/listings/availability` (base URL `https://api.fleetwire.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-listing-availability.md) for the provider-specific parameters and requirements.

