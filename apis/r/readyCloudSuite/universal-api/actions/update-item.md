# ReadyCloud Suite: Update Item

Updates an existing item in ReadyCloud Suite.

```
PUT https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/update-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReadyCloud Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/update-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "boxPk": "string",
  "itemPk": "string",
  "orderPk": "string",
  "orgPk": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/update-item', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "boxPk": "string",
    "itemPk": "string",
    "orderPk": "string",
    "orgPk": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `boxPk` | string | yes | ReadyCloud box identifier. |
| `itemPk` | string | yes | ReadyCloud item identifier. |
| `orderPk` | string | yes | ReadyCloud order identifier. |
| `orgPk` | string | yes | ReadyCloud organization identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "commodity_code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_fields": {},
      "description": "string",
      "ean": "string",
      "export_type_code": "string",
      "image_link": "https://example.com",
      "isbn": "string",
      "joint_production": "string",
      "kind": "string",
      "link": "https://example.com",
      "net_cost_begin_date": "2026-05-07T12:00:00.000Z",
      "net_cost_code": "string",
      "net_cost_end_date": "2026-05-07T12:00:00.000Z",
      "origin_country_code": "string",
      "part_number": "string",
      "pick_location": "string",
      "preference_criteria_code": "string",
      "producer_info_code": "string",
      "quantity": 1,
      "scheduleb_commodity_code": "string",
      "unit_price": "string",
      "unit_weight": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "ups": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `commodity_code` | string |  |
| `created_at` | date |  |
| `custom_fields` | object |  |
| `description` | string |  |
| `ean` | string |  |
| `export_type_code` | string |  |
| `image_link` | string |  |
| `isbn` | string |  |
| `joint_production` | string |  |
| `kind` | string |  |
| `link` | string |  |
| `net_cost_begin_date` | date |  |
| `net_cost_code` | string |  |
| `net_cost_end_date` | date |  |
| `origin_country_code` | string |  |
| `part_number` | string |  |
| `pick_location` | string |  |
| `preference_criteria_code` | string |  |
| `producer_info_code` | string |  |
| `quantity` | number |  |
| `scheduleb_commodity_code` | string |  |
| `unit_price` | string |  |
| `unit_weight` | string |  |
| `updated_at` | date |  |
| `ups` | string |  |
| `url` | string |  |

## Native endpoint

Through the native ReadyCloud Suite API, this operation is `PATCH /api/v2/orgs/:orgPk/orders/:orderPk/boxes/:boxPk/items/:itemPk/` (base URL `https://www.readycloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-item.md) for the provider-specific parameters and requirements.

