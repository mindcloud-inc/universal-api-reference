# FreeAgent: Get Bill

Retrieves detailed bill information from FreeAgent.

```
GET https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/get-bill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreeAgent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/get-bill?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/get-bill?${params}`, {
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
| `id` | string | yes | FreeAgent bill ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "comments": "string",
      "contact": "string",
      "contact_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "dated_on": "2026-05-07T12:00:00.000Z",
      "due_on": "2026-05-07T12:00:00.000Z",
      "due_value": "string",
      "input_total_values_inc_tax": true,
      "is_locked": true,
      "is_paid_by_hire_purchase": true,
      "long_status": "string",
      "native_due_value": "string",
      "net_value": "string",
      "paid_value": "string",
      "project": "string",
      "reference": "string",
      "status": "string",
      "total_value": "string",
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
| `comments` | string |  |
| `contact` | string |  |
| `contact_name` | string |  |
| `created_at` | date |  |
| `currency` | string |  |
| `dated_on` | date |  |
| `due_on` | date |  |
| `due_value` | string |  |
| `input_total_values_inc_tax` | boolean |  |
| `is_locked` | boolean |  |
| `is_paid_by_hire_purchase` | boolean |  |
| `long_status` | string |  |
| `native_due_value` | string |  |
| `net_value` | string |  |
| `paid_value` | string |  |
| `project` | string |  |
| `reference` | string |  |
| `status` | string |  |
| `total_value` | string |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native FreeAgent API, this operation is `GET /bills/:id` (base URL `https://api.freeagent.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bill.md) for the provider-specific parameters and requirements.

