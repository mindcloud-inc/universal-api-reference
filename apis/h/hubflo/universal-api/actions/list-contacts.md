# Hubflo: List Contacts

Retrieves all contact records from Hubflo.

```
GET https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/list-contacts?${params}`, {
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
| `companyId` | string | no |  |
| `contactId` | string | no |  |
| `email` | string | no |  |
| `linkedin` | string | no |  |
| `ownerId` | string | no |  |
| `page` | number | no |  |
| `phone` | string | no |  |
| `projectId` | string | no |  |
| `perPage` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "city": "string",
      "company_id": "string",
      "company_name": "Ava Chen",
      "contact_type": "string",
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "hubspot_id": "string",
      "id": "string",
      "job_title": "string",
      "last_name": "Chen",
      "owner_id": "string",
      "phone": "string",
      "postal_code": "string",
      "priority": "string",
      "secondary_phone": "string",
      "state": "string",
      "tags": [
        "string"
      ],
      "url_linkedin": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `city` | string |  |
| `company_id` | string |  |
| `company_name` | string |  |
| `contact_type` | string |  |
| `country` | string |  |
| `created_at` | date |  |
| `email` | string |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `hubspot_id` | string |  |
| `id` | string |  |
| `job_title` | string |  |
| `last_name` | string |  |
| `owner_id` | string |  |
| `phone` | string |  |
| `postal_code` | string |  |
| `priority` | string |  |
| `secondary_phone` | string |  |
| `state` | string |  |
| `tags` | array<string> |  |
| `url_linkedin` | string |  |

## Native endpoint

Through the native Hubflo API, this operation is `GET /contacts` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

