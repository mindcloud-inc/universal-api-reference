# Rentman: List Equipment Serial Numbers



```
GET https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-equipment-serial-numbers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-equipment-serial-numbers?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-equipment-serial-numbers?${params}`, {
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
      "active": true,
      "asset_location": "string",
      "book_value": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "current_book_value": 1,
      "custom": {},
      "depreciation_monthly": 1,
      "displayname": "Ava Chen",
      "equipment": "string",
      "id": 1,
      "image": "string",
      "last_subproject": "string",
      "modified": "2026-05-07T12:00:00.000Z",
      "next_inspection": "string",
      "purchase_costs": 1,
      "purchasedate": "string",
      "qrcodes": "string",
      "ref": "string",
      "remark": "string",
      "residual_value": 1,
      "sealed": true,
      "serial": "string",
      "tags": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `asset_location` | string |  |
| `book_value` | number |  |
| `created` | date |  |
| `creator` | string |  |
| `current_book_value` | number |  |
| `custom` | object |  |
| `depreciation_monthly` | number |  |
| `displayname` | string |  |
| `equipment` | string |  |
| `id` | number |  |
| `image` | string |  |
| `last_subproject` | string |  |
| `modified` | date |  |
| `next_inspection` | string |  |
| `purchase_costs` | number |  |
| `purchasedate` | string |  |
| `qrcodes` | string |  |
| `ref` | string |  |
| `remark` | string |  |
| `residual_value` | number |  |
| `sealed` | boolean |  |
| `serial` | string |  |
| `tags` | string |  |

## Native endpoint

Through the native Rentman API, this operation is `GET /equipment/:id/serialnumbers` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-equipment-serial-numbers.md) for the provider-specific parameters and requirements.

