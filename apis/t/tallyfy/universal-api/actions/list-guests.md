# Tallyfy: List Guests

Retrieves guests from your Tallyfy organization.

```
GET https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/list-guests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tallyfy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/list-guests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tallyfy/latest/actions/list-guests?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "details": {
        "company_name": "Ava Chen",
        "company_url": "https://example.com",
        "contact_url": "https://example.com",
        "disabled_at": "2026-05-07T12:00:00.000Z",
        "external_sync_source": "string",
        "image_url": "https://example.com",
        "last_city": "string",
        "last_country": "string",
        "opportunity_name": "Ava Chen",
        "opportunity_url": "https://example.com",
        "phone_1": "string",
        "phone_2": "string",
        "reactivated_at": "2026-05-07T12:00:00.000Z",
        "status": "string",
        "timezone": "string"
      },
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "last_accessed_at": "2026-05-07T12:00:00.000Z",
      "last_known_country": "string",
      "last_known_ip": "string",
      "last_name": "Chen",
      "link": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `deleted_at` | date |  |
| `details.company_name` | string |  |
| `details.company_url` | string |  |
| `details.contact_url` | string |  |
| `details.disabled_at` | date |  |
| `details.external_sync_source` | string |  |
| `details.image_url` | string |  |
| `details.last_city` | string |  |
| `details.last_country` | string |  |
| `details.opportunity_name` | string |  |
| `details.opportunity_url` | string |  |
| `details.phone_1` | string |  |
| `details.phone_2` | string |  |
| `details.reactivated_at` | date |  |
| `details.status` | string |  |
| `details.timezone` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `last_accessed_at` | date |  |
| `last_known_country` | string |  |
| `last_known_ip` | string |  |
| `last_name` | string |  |
| `link` | string |  |

## Native endpoint

Through the native Tallyfy API, this operation is `GET /organizations/:org/guests` (base URL `https://api.tallyfy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-guests.md) for the provider-specific parameters and requirements.

