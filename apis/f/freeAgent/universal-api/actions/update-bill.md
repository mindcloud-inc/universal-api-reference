# FreeAgent: Update Bill

Updates an existing bill in FreeAgent.

```
PUT https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-bill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FreeAgent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-bill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freeAgent/latest/actions/update-bill', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | FreeAgent bill ID. |
| `bill` | object | no | Bill payload. |
| `bill.contact` | string | no | Contact being billed. |
| `bill.reference` | string | no | Free-text reference. |
| `bill.dated_on` | date | no | Date of bill. |
| `bill.due_on` | date | no | Due date of bill. |
| `bill.currency` | string | no | Bill currency. |
| `bill.comments` | string | no | Free-text comments. |
| `bill.project` | string | no | Project billed for. |

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

Through the native FreeAgent API, this operation is `PUT /bills/:id` (base URL `https://api.freeagent.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bill.md) for the provider-specific parameters and requirements.

