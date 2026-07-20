# WhatsScale: List CRM Contacts

Retrieves CRM contacts from your WhatsScale account.

```
GET https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/list-crm-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsScale `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/list-crm-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whatsScale/latest/actions/list-crm-contacts?${params}`, {
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
| `limit` | number | no | Results per page, default 50. |
| `page` | number | no | Page number, default 1. |
| `search` | string | no | Search by name or phone. |
| `tag` | string | no | Filter by tag. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasMore": true,
      "items": {
        "created_at": "string",
        "id": "string",
        "name": "Ava Chen",
        "phone": "string",
        "source": "string",
        "tags": [
          "string"
        ],
        "updated_at": "string"
      },
      "limit": 1,
      "page": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasMore` | boolean |  |
| `items` | array<object> |  |
| `items.created_at` | string |  |
| `items.id` | string |  |
| `items.name` | string |  |
| `items.phone` | string |  |
| `items.source` | string |  |
| `items.tags` | array<string> |  |
| `items.updated_at` | string |  |
| `limit` | number |  |
| `page` | number |  |
| `total` | number |  |

## Native endpoint

Through the native WhatsScale API, this operation is `GET /api/crm/contacts` (base URL `https://proxy.whatsscale.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-crm-contacts.md) for the provider-specific parameters and requirements.

