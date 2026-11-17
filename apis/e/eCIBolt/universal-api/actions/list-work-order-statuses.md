# ECI Bolt: List Work Order Statuses



```
GET https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-work-order-statuses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECI Bolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-work-order-statuses?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-work-order-statuses?${params}`, {
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
| `id` | number | yes | Id of the work order. |

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

Through the native ECI Bolt API, this operation is `GET /open/v1/work_orders/:id/statuses` (base URL `https://app.bolttech.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-work-order-statuses.md) for the provider-specific parameters and requirements.

