# Get Orders with BaseLinker

Retrieves orders from BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Get Orders](https://api.baselinker.com/index.php?method=getOrders)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | body | `number` | no | Download one specific order by BaseLinker order identifier. |
| `date_confirmed_from` | body | `number` | no | Unix timestamp for the earliest confirmed order to include. |
| `date_from` | body | `number` | no | Unix timestamp for the earliest order date to include. |
| `id_from` | body | `number` | no | Return orders from this order ID onward. |
| `get_unconfirmed_orders` | body | `boolean` | no | Include orders that are not fully confirmed yet. |
| `status_id` | body | `number` | no | Filter orders by status identifier. |
| `filter_email` | body | `string` | no | Filter orders by customer email address. |
| `filter_order_source` | body | `string` | no | Filter orders by order source code such as ebay or amazon. |
| `filter_order_source_id` | body | `number` | no | Filter orders by the source identifier within the selected order source. |
| `filter_shop_order_id` | body | `number` | no | Return the specific order matching the shop order identifier. |
| `include_custom_extra_fields` | body | `boolean` | no | Include custom additional field values in the response. |
| `include_commission_data` | body | `boolean` | no | Include marketplace commission details for each order. |
| `include_connect_data` | body | `boolean` | no | Include Base Connect contractor data for each order. |
