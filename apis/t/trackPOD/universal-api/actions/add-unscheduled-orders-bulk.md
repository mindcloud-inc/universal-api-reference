# Track-POD: Add Unscheduled Orders Bulk

Creates new unscheduled orders in bulk in Track-POD.

```
POST https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/add-unscheduled-orders-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Track-POD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/add-unscheduled-orders-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/add-unscheduled-orders-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Orders[0].Address` | string | no | First bulk order address. |
| `Orders[0].Client` | string | no | First bulk order client name. |
| `Orders[0].ContactName` | string | no | First bulk order contact name. |
| `Orders[0].Date` | string | no | First bulk order date and time. |
| `Orders[0].Number` | string | no | First bulk order number. |
| `Orders[0].Phone` | string | no | First bulk order phone number. |
| `Orders[0].TimeSlotFrom` | string | no | First bulk order time window start. |
| `Orders[0].TimeSlotTo` | string | no | First bulk order time window end. |
| `Orders[1].Address` | string | no | Second bulk order address. |
| `Orders[1].Client` | string | no | Second bulk order client name. |
| `Orders[1].ContactName` | string | no | Second bulk order contact name. |
| `Orders[1].Date` | string | no | Second bulk order date and time. |
| `Orders[1].Number` | string | no | Second bulk order number. |
| `Orders[1].Phone` | string | no | Second bulk order phone number. |
| `Orders[1].TimeSlotFrom` | string | no | Second bulk order time window start. |
| `Orders[1].TimeSlotTo` | string | no | Second bulk order time window end. |
| `Orders[2].Address` | string | no | Third bulk order address. |
| `Orders[2].Client` | string | no | Third bulk order client name. |
| `Orders[2].ContactName` | string | no | Third bulk order contact name. |
| `Orders[2].Date` | string | no | Third bulk order date and time. |
| `Orders[2].Number` | string | no | Third bulk order number. |
| `Orders[2].Phone` | string | no | Third bulk order phone number. |
| `Orders[2].TimeSlotFrom` | string | no | Third bulk order time window start. |
| `Orders[2].TimeSlotTo` | string | no | Third bulk order time window end. |
| `updateAddressGps` | boolean | no | Force-update existing address latitude/longitude from each payload order. Default: `false`. |
| `updateGoodsPrice` | boolean | no | Force-update existing goods prices from each payload order. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Detail": "string",
      "Status": 1,
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Detail` | string | A human-readable explanation specific to this response. |
| `Status` | number | The HTTP status code for the response |
| `Title` | string | A short, human-readable summary of the response |

## Native endpoint

Through the native Track-POD API, this operation is `POST /Order/Bulk` (base URL `https://api.track-pod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-unscheduled-orders-bulk.md) for the provider-specific parameters and requirements.

