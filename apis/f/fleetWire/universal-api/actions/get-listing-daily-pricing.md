# FleetWire: Get Listing Daily Pricing

Retrieves listing daily pricing from FleetWire.

```
GET https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-listing-daily-pricing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FleetWire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-listing-daily-pricing?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetWire/latest/actions/get-listing-daily-pricing?${params}`, {
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
| `end` | string | no | End datetime for daily pricing. |
| `listingId` | string | no | The FleetWire listing identifier. |
| `start` | string | no | Start datetime for daily pricing. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dailyPricing": [
        {}
      ],
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dailyPricing` | array<object> | Per-day pricing rows for the requested listing and date range. |
| `success` | boolean | Whether FleetWire returned daily pricing successfully. |

## Native endpoint

Through the native FleetWire API, this operation is `GET /api/v2/listings/:l_id/daily_pricing` (base URL `https://api.fleetwire.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-listing-daily-pricing.md) for the provider-specific parameters and requirements.

