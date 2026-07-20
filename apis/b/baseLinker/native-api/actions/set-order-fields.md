# Set Order Fields with BaseLinker

Updates order fields in BaseLinker.

## Endpoint

- **Method:** `POST`
- **Path:** `/connector.php`
- **Base URL:** `https://api.baselinker.com`
- **Official documentation:** [Set Order Fields](https://api.baselinker.com/index.php?method=setOrderFields)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `order_id` | body | `number` | yes | Order identifier from the BaseLinker order manager. |
| `user_comments` | body | `string` | no | Customer-visible order comments. |
| `admin_comments` | body | `string` | no | Internal admin comments for the order. |
| `email` | body | `string` | no | Customer email address. |
| `phone` | body | `string` | no | Customer phone number. |
| `delivery_method` | body | `string` | no | Delivery method name visible on the order. |
| `delivery_price` | body | `number` | no | Delivery price value. |
| `pick_state` | body | `boolean` | no | Picking state flag. |
| `pack_state` | body | `boolean` | no | Packing state flag. |
| `star` | body | `number` | no | Star marker value from 0 to 3. |
| `parameters` | body | `object` | no | Optional raw BaseLinker parameters merged with the typed fields before request serialization. |
