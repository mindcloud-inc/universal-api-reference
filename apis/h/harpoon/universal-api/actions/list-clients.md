# Harpoon: List Clients

Retrieves clients from Harpoon.

```
GET https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harpoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/list-clients?${params}`, {
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
| `select` | string | no | If present, returns simplified data for dropdown usage. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "average_days_to_pay": 1,
      "collected_total": 1,
      "contacts": [
        {}
      ],
      "credit_available": 1,
      "estimates_count": 1,
      "id": 1,
      "invoices_count": 1,
      "name": "Ava Chen",
      "other_income_count": 1,
      "outstanding_total": 1,
      "projects_count": 1,
      "sent_total": 1,
      "source": "string",
      "status": {},
      "tax_name": "Ava Chen",
      "tax_number": "string",
      "team_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `average_days_to_pay` | number |  |
| `collected_total` | number |  |
| `contacts` | array<object> |  |
| `credit_available` | number |  |
| `estimates_count` | number |  |
| `id` | number |  |
| `invoices_count` | number |  |
| `name` | string |  |
| `other_income_count` | number |  |
| `outstanding_total` | number |  |
| `projects_count` | number |  |
| `sent_total` | number |  |
| `source` | string |  |
| `status` | object |  |
| `tax_name` | string |  |
| `tax_number` | string |  |
| `team_id` | number |  |

## Native endpoint

Through the native Harpoon API, this operation is `GET /clients` (base URL `https://app.harpoonapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

