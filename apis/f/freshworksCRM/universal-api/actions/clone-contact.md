# Freshworks CRM: Clone Contact

Creates a contact by cloning one in Freshworks CRM.

```
POST https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/clone-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/clone-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/clone-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contact` | string | no |  |
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact": {
        "address": "string",
        "avatar": "string",
        "city": "string",
        "country": "string",
        "display_name": "Ava Chen",
        "email": "ava@example.com",
        "facebook": "string",
        "first_name": "Ava",
        "id": 1,
        "job_title": "string",
        "keyword": "string",
        "last_contacted": "2026-05-07T12:00:00.000Z",
        "last_name": "Chen",
        "last_seen": "2026-05-07T12:00:00.000Z",
        "lead_score": 1,
        "linkedin": "https://example.com",
        "links": {
          "activities": "https://example.com",
          "conversations": "https://example.com"
        },
        "medium": "string",
        "mobile_number": "string",
        "open_deals_amount": "string",
        "state": "string",
        "time_zone": "string",
        "twitter": "string",
        "updated_at": "2026-05-07T12:00:00.000Z",
        "work_number": "string",
        "zipcode": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact.address` | string |  |
| `contact.avatar` | string |  |
| `contact.city` | string |  |
| `contact.country` | string |  |
| `contact.display_name` | string |  |
| `contact.email` | string |  |
| `contact.facebook` | string |  |
| `contact.first_name` | string |  |
| `contact.id` | number |  |
| `contact.job_title` | string |  |
| `contact.keyword` | string |  |
| `contact.last_contacted` | date |  |
| `contact.last_name` | string |  |
| `contact.last_seen` | date |  |
| `contact.lead_score` | number |  |
| `contact.linkedin` | string |  |
| `contact.links.activities` | string |  |
| `contact.links.conversations` | string |  |
| `contact.medium` | string |  |
| `contact.mobile_number` | string |  |
| `contact.open_deals_amount` | string |  |
| `contact.state` | string |  |
| `contact.time_zone` | string |  |
| `contact.twitter` | string |  |
| `contact.updated_at` | date |  |
| `contact.work_number` | string |  |
| `contact.zipcode` | string |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/contacts/:id/clone` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clone-contact.md) for the provider-specific parameters and requirements.

