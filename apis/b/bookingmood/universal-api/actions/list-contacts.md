# Bookingmood: List Contacts

Retrieves contact records from the Bookingmood API.

```
GET https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookingmood `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/list-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "avatar": "string",
      "city": "string",
      "company_name": "Ava Chen",
      "country": "string",
      "country_code": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "creator_id": "string",
      "e_invoice_address": "string",
      "e_invoice_scheme": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "language": "string",
      "last_name": "Chen",
      "meta": [
        {}
      ],
      "name": "Ava Chen",
      "notes": "string",
      "organization_id": "string",
      "phone": "string",
      "province": "string",
      "state": "string",
      "street": "string",
      "street2": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `avatar` | string |  |
| `city` | string |  |
| `company_name` | string |  |
| `country` | string |  |
| `country_code` | string |  |
| `created_at` | date |  |
| `creator_id` | string |  |
| `e_invoice_address` | string |  |
| `e_invoice_scheme` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `language` | string |  |
| `last_name` | string |  |
| `meta` | array<object> |  |
| `name` | string |  |
| `notes` | string |  |
| `organization_id` | string |  |
| `phone` | string |  |
| `province` | string |  |
| `state` | string |  |
| `street` | string |  |
| `street2` | string |  |
| `updated_at` | date |  |
| `zip` | string |  |

## Native endpoint

Through the native Bookingmood API, this operation is `GET /contacts` (base URL `https://api.bookingmood.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

