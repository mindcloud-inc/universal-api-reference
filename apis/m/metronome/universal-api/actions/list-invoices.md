# Metronome: List Invoices

Retrieves invoices from Metronome.

```
GET https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metronome `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0&customerId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "customerId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metronome/latest/actions/list-invoices?${params}`, {
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
| `customerId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable_status": "string",
      "contract_id": "string",
      "credit_type": {
        "id": "string",
        "name": "Ava Chen"
      },
      "customer_id": "string",
      "end_timestamp": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "issued_at": "2026-05-07T12:00:00.000Z",
      "line_items": [
        {
          "credit_type": {
            "id": "string",
            "name": "Ava Chen"
          },
          "ending_before": "2026-05-07T12:00:00.000Z",
          "is_prorated": true,
          "name": "Ava Chen",
          "product_id": "string",
          "product_type": "string",
          "quantity": 1,
          "starting_at": "2026-05-07T12:00:00.000Z",
          "subscription_id": "string",
          "total": 1,
          "type": "string",
          "unit_price": 1
        }
      ],
      "start_timestamp": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "total": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable_status` | string |  |
| `contract_id` | string |  |
| `credit_type.id` | string |  |
| `credit_type.name` | string |  |
| `customer_id` | string |  |
| `end_timestamp` | date |  |
| `id` | string |  |
| `issued_at` | date |  |
| `line_items[].credit_type.id` | string |  |
| `line_items[].credit_type.name` | string |  |
| `line_items[].ending_before` | date |  |
| `line_items[].is_prorated` | boolean |  |
| `line_items[].name` | string |  |
| `line_items[].product_id` | string |  |
| `line_items[].product_type` | string |  |
| `line_items[].quantity` | number |  |
| `line_items[].starting_at` | date |  |
| `line_items[].subscription_id` | string |  |
| `line_items[].total` | number |  |
| `line_items[].type` | string |  |
| `line_items[].unit_price` | number |  |
| `start_timestamp` | date |  |
| `status` | string |  |
| `total` | number |  |
| `type` | string |  |

## Native endpoint

Through the native Metronome API, this operation is `GET /v1/customers/:customer_id/invoices` (base URL `https://api.metronome.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

