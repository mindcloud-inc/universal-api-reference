# Track-POD: Add Existing Order To Route

Updates a Track-POD route by adding an existing order.

```
PUT https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/add-existing-order-to-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Track-POD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/add-existing-order-to-route" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "route-1001",
  "orderId": "31cc9a7a-5658-4f7a-8c7c-99fe7f7173d6"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/add-existing-order-to-route', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "route-1001",
    "orderId": "31cc9a7a-5658-4f7a-8c7c-99fe7f7173d6"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `allowReschedule` | boolean | no | Allow rescheduling and transferring an order with failed delivery status from another route. Default: `false`. |
| `allowTransfer` | boolean | no | Allow transferring an order without delivery status from another route. Default: `false`. |
| `id` | string | yes | Track-POD unique identifier for the route. Example: `route-1001`. |
| `orderId` | string | yes | Track-POD unique identifier for the order. Example: `31cc9a7a-5658-4f7a-8c7c-99fe7f7173d6`. |

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

Through the native Track-POD API, this operation is `PUT /Route/Id/:id/Order/Id/:orderId` (base URL `https://api.track-pod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-existing-order-to-route.md) for the provider-specific parameters and requirements.

