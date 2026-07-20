# Rentman: List Project Equipment



```
GET https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-project-equipment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-project-equipment?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-project-equipment?${params}`, {
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
| `id` | number | yes | Numeric Rentman project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "custom": {},
      "delay_notified": true,
      "discount": 1,
      "displayname": "Ava Chen",
      "equipment": "string",
      "equipment_group": "string",
      "external_remark": "string",
      "factor": 1,
      "has_missings": true,
      "id": 1,
      "internal_remark": "string",
      "is_option": true,
      "ledger": "string",
      "ledger_debit": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "order": 1,
      "parent": "string",
      "planperiod_end": "2026-05-07T12:00:00.000Z",
      "planperiod_start": "2026-05-07T12:00:00.000Z",
      "quantity": 1,
      "quantity_total": 1,
      "serial_number_ids": "string",
      "subrent_reservations": 1,
      "unit_price": 1,
      "updateHash": "string",
      "warehouse_reservations": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `creator` | string |  |
| `custom` | object |  |
| `delay_notified` | boolean |  |
| `discount` | number |  |
| `displayname` | string |  |
| `equipment` | string |  |
| `equipment_group` | string |  |
| `external_remark` | string |  |
| `factor` | number |  |
| `has_missings` | boolean |  |
| `id` | number |  |
| `internal_remark` | string |  |
| `is_option` | boolean |  |
| `ledger` | string |  |
| `ledger_debit` | string |  |
| `modified` | date |  |
| `name` | string |  |
| `order` | number |  |
| `parent` | string |  |
| `planperiod_end` | date |  |
| `planperiod_start` | date |  |
| `quantity` | number |  |
| `quantity_total` | number |  |
| `serial_number_ids` | string |  |
| `subrent_reservations` | number |  |
| `unit_price` | number |  |
| `updateHash` | string |  |
| `warehouse_reservations` | number |  |

## Native endpoint

Through the native Rentman API, this operation is `GET /projects/:id/projectequipment` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-equipment.md) for the provider-specific parameters and requirements.

