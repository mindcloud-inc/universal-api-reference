# Hubflo: Create Company

Creates a new company in Hubflo.

```
POST https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hubflo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubflo/latest/actions/create-company', {
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
| `address` | string | no |  |
| `city` | string | no |  |
| `country` | string | no |  |
| `email` | string | no |  |
| `hubspotId` | string | no |  |
| `name` | string | yes |  |
| `ownerId` | string | no |  |
| `postalCode` | string | no |  |
| `siret` | string | no |  |
| `staff` | string | no |  |
| `state` | string | no |  |
| `urlLinkedin` | string | no |  |
| `vatNumber` | string | no |  |
| `website` | string | no |  |
| `businessDescription` | string | no |  |
| `tags` | list<string> | no |  |

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

Through the native Hubflo API, this operation is `POST /companies` (base URL `https://app.hubflo.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-company.md) for the provider-specific parameters and requirements.

