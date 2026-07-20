# EventGeek: List Event Expenses

Retrieves event expense records from EventGeek.

```
GET https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/list-event-expenses
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EventGeek `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/list-event-expenses?connectionId=$CONNECTION_ID&event_id=RXZlbnQtNzg5NDE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "event_id": "RXZlbnQtNzg5NDE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventGeek/latest/actions/list-event-expenses?${params}`, {
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
| `event_id` | string | yes | Circa event identifier. Default: `RXZlbnQtNzg5NDE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "category": "string",
      "created_at": "string",
      "description": "string",
      "event_id": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `category` | string |  |
| `created_at` | string |  |
| `description` | string |  |
| `event_id` | string |  |
| `id` | string |  |

## Native endpoint

Through the native EventGeek API, this operation is `GET /events/:event_id/expenses` (base URL `https://app.circa.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-expenses.md) for the provider-specific parameters and requirements.

