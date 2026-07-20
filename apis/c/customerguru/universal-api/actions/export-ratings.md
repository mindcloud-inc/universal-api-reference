# Customer.guru: Export Ratings

Retrieves customer ratings from Customer.guru.

```
GET https://connect.mindcloud.co/v1/universal/customerguru/latest/actions/export-ratings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Customer.guru `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerguru/latest/actions/export-ratings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerguru/latest/actions/export-ratings?${params}`, {
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
      "city": "string",
      "country": "string",
      "email": "ava@example.com",
      "email_clicked_at": "2026-05-07T12:00:00.000Z",
      "email_opened_at": "2026-05-07T12:00:00.000Z",
      "email_sent_at": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "ip_address": "string",
      "message": "string",
      "score": 1,
      "state": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `country` | string |  |
| `email` | string |  |
| `email_clicked_at` | date |  |
| `email_opened_at` | date |  |
| `email_sent_at` | date |  |
| `id` | number |  |
| `ip_address` | string |  |
| `message` | string |  |
| `score` | number |  |
| `state` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Customer.guru API, this operation is `GET /export/ratings` (base URL `https://customer.guru`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/export-ratings.md) for the provider-specific parameters and requirements.

