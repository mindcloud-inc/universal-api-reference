# FleetWire: Get Listing

Retrieves a listing from FleetWire.

```
GET https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-listing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FleetWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-listing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-listing?${params}`, {
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
| `listingId` | string | no | The FleetWire listing identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "listing": {},
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `listing` | object | Requested listing payload. |
| `success` | boolean | Whether FleetWire returned the listing successfully. |

## Native endpoint

Through the native FleetWire API, this operation is `GET /api/v2/listings/:l_id` (base URL `https://api.fleetwire.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-listing.md) for the provider-specific parameters and requirements.

