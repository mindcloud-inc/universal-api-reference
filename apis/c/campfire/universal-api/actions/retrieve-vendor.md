# Campfire: Retrieve Vendor

Retrieves a vendor from Campfire.

```
GET https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-vendor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Campfire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-vendor?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/campfire/latest/actions/retrieve-vendor?${params}`, {
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
| `id` | number | yes | The vendor ID to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "company_name": "Ava Chen",
      "contacts": [
        {}
      ],
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "customer": 1,
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "external_id": "string",
      "id": 1,
      "is_1099": true,
      "is_deleted": true,
      "last_modified_at": "2026-05-07T12:00:00.000Z",
      "lineage_array": [
        "string"
      ],
      "name": "Ava Chen",
      "notes": "string",
      "parent": 1,
      "parent_name": "Ava Chen",
      "payment_term": 1,
      "phone_number": "string",
      "source": "string",
      "state": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `company_name` | string |  |
| `contacts` | array<object> |  |
| `country` | string |  |
| `created_at` | date |  |
| `customer` | number |  |
| `deleted_at` | date |  |
| `email` | string |  |
| `external_id` | string |  |
| `id` | number |  |
| `is_1099` | boolean |  |
| `is_deleted` | boolean |  |
| `last_modified_at` | date |  |
| `lineage_array` | array<string> |  |
| `name` | string |  |
| `notes` | string |  |
| `parent` | number |  |
| `parent_name` | string |  |
| `payment_term` | number |  |
| `phone_number` | string |  |
| `source` | string |  |
| `state` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Campfire API, this operation is `GET /coa/api/vendor/:id` (base URL `https://api.meetcampfire.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-vendor.md) for the provider-specific parameters and requirements.

