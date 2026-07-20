# ReadyCloud Suite: Update Order

Updates an existing order in ReadyCloud Suite.

```
PUT https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/update-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ReadyCloud Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/update-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "orderPk": "string",
  "orgPk": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/readyCloudSuite/latest/actions/update-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `orderPk` | string | yes | ReadyCloud order identifier. |
| `orgPk` | string | yes | ReadyCloud organization identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billing": {},
      "boxes": [
        {}
      ],
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_fields": {},
      "customer_number": "string",
      "message": "string",
      "nested_updated_at": "2026-05-07T12:00:00.000Z",
      "notes": [
        {}
      ],
      "order_number": "string",
      "ordered_at": "2026-05-07T12:00:00.000Z",
      "po_number": "string",
      "primary_id": "string",
      "printed_at": "2026-05-07T12:00:00.000Z",
      "relations": [
        {}
      ],
      "shipping": {},
      "source": {},
      "tags": [
        {}
      ],
      "terms": "string",
      "unique_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billing` | object |  |
| `boxes` | array<object> |  |
| `created_at` | date |  |
| `custom_fields` | object |  |
| `customer_number` | string |  |
| `message` | string |  |
| `nested_updated_at` | date |  |
| `notes` | array<object> |  |
| `order_number` | string |  |
| `ordered_at` | date |  |
| `po_number` | string |  |
| `primary_id` | string |  |
| `printed_at` | date |  |
| `relations` | array<object> |  |
| `shipping` | object |  |
| `source` | object |  |
| `tags` | array<object> |  |
| `terms` | string |  |
| `unique_id` | string |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native ReadyCloud Suite API, this operation is `PATCH /api/v2/orgs/:orgPk/orders/:orderPk/` (base URL `https://www.readycloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-order.md) for the provider-specific parameters and requirements.

