# ECI Bolt: Update Work Order Status



```
PUT https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/update-work-order-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECI Bolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/update-work-order-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/update-work-order-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Id of the work order. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | boolean | no |  |
| `workOrderStatusTypeId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "id": 1,
      "status": true,
      "updatedAt": "string",
      "workOrderId": 1,
      "workOrderStatusTypeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `id` | number |  |
| `status` | boolean |  |
| `updatedAt` | string |  |
| `workOrderId` | number |  |
| `workOrderStatusTypeId` | number |  |

## Native endpoint

Through the native ECI Bolt API, this operation is `PATCH /open/v1/work_orders/:id/statuses` (base URL `https://app.bolttech.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-work-order-status.md) for the provider-specific parameters and requirements.

