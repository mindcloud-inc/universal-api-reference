# BaseLinker: Get Orders

Retrieves orders from BaseLinker.

```
GET https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BaseLinker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/baseLinker/latest/actions/get-orders?${params}`, {
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
| `order_id` | number | no | Download one specific order by BaseLinker order identifier. |
| `date_confirmed_from` | number | no | Unix timestamp for the earliest confirmed order to include. |
| `date_from` | number | no | Unix timestamp for the earliest order date to include. |
| `id_from` | number | no | Return orders from this order ID onward. |
| `get_unconfirmed_orders` | boolean | no | Include orders that are not fully confirmed yet. |
| `status_id` | number | no | Filter orders by status identifier. |
| `filter_email` | string | no | Filter orders by customer email address. |
| `filter_order_source` | string | no | Filter orders by order source code such as ebay or amazon. |
| `filter_order_source_id` | number | no | Filter orders by the source identifier within the selected order source. |
| `filter_shop_order_id` | number | no | Return the specific order matching the shop order identifier. |
| `include_custom_extra_fields` | boolean | no | Include custom additional field values in the response. |
| `include_commission_data` | boolean | no | Include marketplace commission details for each order. |
| `include_connect_data` | boolean | no | Include Base Connect contractor data for each order. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BaseLinker API returns.

## Native endpoint

Through the native BaseLinker API, this operation is `POST /connector.php` (base URL `https://api.baselinker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-orders.md) for the provider-specific parameters and requirements.

