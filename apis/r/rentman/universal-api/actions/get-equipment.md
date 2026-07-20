# Rentman: Get Equipment



```
GET https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-equipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-equipment?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/get-equipment?${params}`, {
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
| `id` | number | yes | Numeric Rentman equipment identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "can_edit_content_during_planning": true,
      "code": "string",
      "country_of_origin": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "critical_stock_level": 1,
      "current": 1,
      "current_quantity": 1,
      "current_quantity_excl_cases": 1,
      "custom": {},
      "defaultgroup": "string",
      "displayname": "Ava Chen",
      "empty_weight": 1,
      "external_remark": "string",
      "factor_group": "string",
      "folder": "string",
      "height": 1,
      "id": 1,
      "image": "string",
      "in_archive": true,
      "in_planner": true,
      "in_shop": true,
      "internal_remark": "string",
      "is_combination": true,
      "is_physical": "string",
      "ledger": "string",
      "ledger_debit": "string",
      "length": 1,
      "list_price": 1,
      "location_in_warehouse": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "packed_per": 1,
      "power": 1,
      "price": 1,
      "qrcodes": "string",
      "qrcodes_of_serial_numbers": "string",
      "quantity_in_cases": 1,
      "rental_sales": "string",
      "shop_description_long": "string",
      "shop_description_short": "string",
      "shop_featured": true,
      "stock_management": "string",
      "strict_container_content": "string",
      "subrental_costs": 1,
      "surface_article": true,
      "tags": "string",
      "taxclass": "string",
      "temporary": true,
      "type": "string",
      "unit": "string",
      "updateHash": "string",
      "volume": 1,
      "weight": 1,
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `can_edit_content_during_planning` | boolean |  |
| `code` | string |  |
| `country_of_origin` | string |  |
| `created` | date |  |
| `critical_stock_level` | number |  |
| `current` | number |  |
| `current_quantity` | number |  |
| `current_quantity_excl_cases` | number |  |
| `custom` | object |  |
| `defaultgroup` | string |  |
| `displayname` | string |  |
| `empty_weight` | number |  |
| `external_remark` | string |  |
| `factor_group` | string |  |
| `folder` | string |  |
| `height` | number |  |
| `id` | number |  |
| `image` | string |  |
| `in_archive` | boolean |  |
| `in_planner` | boolean |  |
| `in_shop` | boolean |  |
| `internal_remark` | string |  |
| `is_combination` | boolean |  |
| `is_physical` | string |  |
| `ledger` | string |  |
| `ledger_debit` | string |  |
| `length` | number |  |
| `list_price` | number |  |
| `location_in_warehouse` | string |  |
| `modified` | date |  |
| `name` | string |  |
| `packed_per` | number |  |
| `power` | number |  |
| `price` | number |  |
| `qrcodes` | string |  |
| `qrcodes_of_serial_numbers` | string |  |
| `quantity_in_cases` | number |  |
| `rental_sales` | string |  |
| `shop_description_long` | string |  |
| `shop_description_short` | string |  |
| `shop_featured` | boolean |  |
| `stock_management` | string |  |
| `strict_container_content` | string |  |
| `subrental_costs` | number |  |
| `surface_article` | boolean |  |
| `tags` | string |  |
| `taxclass` | string |  |
| `temporary` | boolean |  |
| `type` | string |  |
| `unit` | string |  |
| `updateHash` | string |  |
| `volume` | number |  |
| `weight` | number |  |
| `width` | number |  |

## Native endpoint

Through the native Rentman API, this operation is `GET /equipment/:id` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-equipment.md) for the provider-specific parameters and requirements.

