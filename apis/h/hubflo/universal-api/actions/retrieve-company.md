# Hubflo: Retrieve Company

Retrieves a company from Hubflo by ID.

```
GET https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-company?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/retrieve-company?${params}`, {
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
      "business_description": "string",
      "city": "string",
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "hubspot_id": "string",
      "id": "string",
      "name": "Ava Chen",
      "owner_id": "string",
      "parent_id": "string",
      "postal_code": "string",
      "siret": "string",
      "staff": "string",
      "state": "string",
      "tags": [
        "string"
      ],
      "url_linkedin": "https://example.com",
      "vat_number": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `business_description` | string |  |
| `city` | string |  |
| `country` | string |  |
| `created_at` | date |  |
| `email` | string |  |
| `hubspot_id` | string |  |
| `id` | string |  |
| `name` | string |  |
| `owner_id` | string |  |
| `parent_id` | string |  |
| `postal_code` | string |  |
| `siret` | string |  |
| `staff` | string |  |
| `state` | string |  |
| `tags` | array<string> |  |
| `url_linkedin` | string |  |
| `vat_number` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Hubflo API, this operation is `GET /companies/:id` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-company.md) for the provider-specific parameters and requirements.

