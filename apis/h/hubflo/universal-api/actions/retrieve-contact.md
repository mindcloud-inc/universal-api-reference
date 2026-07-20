# Hubflo: Retrieve Contact

Retrieves a contact from Hubflo by ID.

```
GET https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-contact?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Hubflo API, this operation is `GET /contacts/:id` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-contact.md) for the provider-specific parameters and requirements.

