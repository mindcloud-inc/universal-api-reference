# Craftboxx: Create Customer

Creates a customer in Craftboxx.

```
POST https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Craftboxx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The customer name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "customer_number": "string",
      "first_line": "string",
      "id": 1,
      "info": "string",
      "interfaces": [
        "string"
      ],
      "name": "Ava Chen",
      "planner_changelog_url": "https://example.com",
      "planner_delete_url": "https://example.com",
      "planner_details_url": "https://example.com",
      "planner_edit_url": "https://example.com",
      "second_line": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Creation timestamp. |
| `customer_number` | string | Customer number. |
| `first_line` | string | Primary display line. |
| `id` | number | Customer ID. |
| `info` | string | Additional customer info. |
| `interfaces` | array<string> | Available interface flags. |
| `name` | string | Customer name. |
| `planner_changelog_url` | string | Planner changelog URL. |
| `planner_delete_url` | string | Planner delete URL. |
| `planner_details_url` | string | Planner details URL. |
| `planner_edit_url` | string | Planner edit URL. |
| `second_line` | string | Secondary display line. |
| `updated_at` | date | Update timestamp. |

## Native endpoint

Through the native Craftboxx API, this operation is `POST customers` (base URL `https://api.craftboxx.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

