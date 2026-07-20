# Harpoon: Update Client

Updates an existing client in Harpoon.

```
PUT https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/update-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harpoon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/update-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harpoon/latest/actions/update-client', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Client ID. |
| `clientName` | string | no |  |
| `source` | string | no |  |
| `address` | string | no |  |
| `taxName` | string | no |  |
| `taxNumber` | string | no |  |
| `language` | string | no |  |
| `contacts[]` | array<object> | no |  |

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

Through the native Harpoon API, this operation is `PUT /clients/:id` (base URL `https://app.harpoonapp.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-client.md) for the provider-specific parameters and requirements.

