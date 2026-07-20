# Customer.guru: Export Customers

Retrieves customers from Customer.guru.

```
GET https://connect.mindcloud.co/v1/universal/customerguru/latest/actions/export-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.guru `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerguru/latest/actions/export-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerguru/latest/actions/export-customers?${params}`, {
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
| `page` | number | no | Zero-based export page number. Default: `0`. |
| `perPage` | number | no | Number of rows to export per page. Default: `50`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "message": "string",
      "rated_at": "2026-05-07T12:00:00.000Z",
      "score": 1,
      "unsubscribed_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `email` | string |  |
| `id` | number |  |
| `message` | string |  |
| `rated_at` | date |  |
| `score` | number |  |
| `unsubscribed_at` | date |  |

## Native endpoint

Through the native Customer.guru API, this operation is `GET /export/customers` (base URL `https://customer.guru`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/export-customers.md) for the provider-specific parameters and requirements.

