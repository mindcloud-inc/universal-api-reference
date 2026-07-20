# Hubflo: Update Contact

Updates an existing contact in Hubflo.

```
PUT https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/update-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/update-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "firstName": "Ava",
  "lastName": "Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/update-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "firstName": "Ava",
    "lastName": "Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no |  |
| `city` | string | no |  |
| `companyId` | string | no |  |
| `companyName` | string | no |  |
| `contactType` | string | no |  |
| `country` | string | no |  |
| `email` | string | no |  |
| `fullName` | string | no |  |
| `hubspotId` | string | no |  |
| `id` | string | yes |  |
| `jobTitle` | string | no |  |
| `ownerEmail` | string | no |  |
| `ownerId` | string | no |  |
| `phone` | string | no |  |
| `postalCode` | string | no |  |
| `priority` | string | no |  |
| `secondaryPhone` | string | no |  |
| `state` | string | no |  |
| `urlLinkedin` | string | no |  |
| `firstName` | string | yes |  |
| `lastName` | string | yes |  |
| `tags` | list<string> | no |  |

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

Through the native Hubflo API, this operation is `PATCH /contacts/:id` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-contact.md) for the provider-specific parameters and requirements.

