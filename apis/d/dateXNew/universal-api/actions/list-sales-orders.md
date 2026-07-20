# DateX: List Sales Orders



```
GET https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-sales-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DateX `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-sales-orders?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dateXNew/latest/actions/list-sales-orders?${params}`, {
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
| `filters.owner` | string | no | Owner filter. |
| `filters.project` | string | no | Project filter. |
| `filters.warehouse` | string | no | Warehouse filter. |
| `filters.status` | string | no | Status filter. |
| `filters.lookup` | string | no | Sales order lookup filter. |
| `filters.orderId` | number | no | Numeric order ID filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "carrier": "string",
      "createdOn": "string",
      "fulfilledOn": "string",
      "lookup": "string",
      "orderId": 1,
      "orderLines": [
        {}
      ],
      "owner": "string",
      "project": "string",
      "shipments": [
        {}
      ],
      "status": "string",
      "warehouse": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `carrier` | string |  |
| `createdOn` | string |  |
| `fulfilledOn` | string |  |
| `lookup` | string |  |
| `orderId` | number |  |
| `orderLines` | array<object> |  |
| `owner` | string |  |
| `project` | string |  |
| `shipments` | array<object> |  |
| `status` | string |  |
| `warehouse` | string |  |

## Native endpoint

Through the native DateX API, this operation is `POST sales_orders/get` (base URL `https://{{credentials.environment}}.wavelength.host/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sales-orders.md) for the provider-specific parameters and requirements.

