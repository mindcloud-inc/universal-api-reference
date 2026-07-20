# Rithum DSCO: List Orders

Lists orders in Rithum DSCO.

```
GET https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rithum DSCO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rithumDSCOV2/latest/actions/list-orders?${params}`, {
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
| `consumerOrderNumber` | string | no | Filter orders by consumer order number. |
| `ordersCreatedSince` | date | no | Filter to orders created since this timestamp. |
| `ordersUpdatedSince` | date | no | Filter to orders updated since this timestamp. |
| `until` | date | no | Upper timestamp bound for the order query. |
| `status` | string | no | Filter orders by DSCO order status. |
| `includeTestOrders` | boolean | no | Whether DSCO should include test orders in the response. |
| `returnedOnly` | boolean | no | Whether to return only orders with returns. |
| `ordersPerPage` | number | no | Maximum number of orders to return in the page. |
| `lifecycle` | string | no | Filter orders by lifecycle. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scrollId` | string | no | Pagination scroll identifier returned by a prior DSCO orders page response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orders": [
        {}
      ],
      "scrollId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orders` | array<object> | Orders returned by the DSCO order page query. |
| `scrollId` | string | Scroll identifier used to fetch the next page of DSCO order results. |

## Native endpoint

Through the native Rithum DSCO API, this operation is `GET order/page` (base URL `https://api.dsco.io/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

