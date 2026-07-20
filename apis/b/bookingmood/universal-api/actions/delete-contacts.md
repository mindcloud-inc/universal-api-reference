# Bookingmood: Delete Contacts

Deletes contact records from the Bookingmood API.

```
DELETE https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/delete-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookingmood `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/delete-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookingmood/latest/actions/delete-contacts?${params}`, {
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

Through the native Bookingmood API, this operation is `DELETE /contacts` (base URL `https://api.bookingmood.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-contacts.md) for the provider-specific parameters and requirements.

