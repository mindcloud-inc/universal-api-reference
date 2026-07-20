# Metronome: Search Events

Finds events in Metronome by transaction ID.

```
GET https://connect.mindcloud.co/v1/universal/metronome/latest/actions/search-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Metronome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/metronome/latest/actions/search-events?connectionId=$CONNECTION_ID&transactionIds%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "transactionIds[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/metronome/latest/actions/search-events?${params}`, {
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
| `transactionIds[]` | array<string> | yes | The transaction IDs of the events to retrieve. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "billable_metrics": [
        {
          "aggregation_type": "string",
          "id": "string",
          "name": "Ava Chen"
        }
      ],
      "customer_id": "string",
      "event_type": "string",
      "id": "string",
      "is_duplicate": true,
      "matched_customer": {
        "id": "string",
        "name": "Ava Chen"
      },
      "processed_at": "2026-05-07T12:00:00.000Z",
      "properties": {
        "quantity": "string"
      },
      "timestamp": "2026-05-07T12:00:00.000Z",
      "transaction_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billable_metrics[].aggregation_type` | string |  |
| `billable_metrics[].id` | string |  |
| `billable_metrics[].name` | string |  |
| `customer_id` | string |  |
| `event_type` | string |  |
| `id` | string |  |
| `is_duplicate` | boolean |  |
| `matched_customer.id` | string |  |
| `matched_customer.name` | string |  |
| `processed_at` | date |  |
| `properties.quantity` | string |  |
| `timestamp` | date |  |
| `transaction_id` | string |  |

## Native endpoint

Through the native Metronome API, this operation is `POST /v1/events/search` (base URL `https://api.metronome.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-events.md) for the provider-specific parameters and requirements.

