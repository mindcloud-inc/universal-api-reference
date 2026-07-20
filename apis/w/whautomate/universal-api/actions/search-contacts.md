# Whautomate: Search Contacts

Finds matching contacts in Whautomate.

```
GET https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Whautomate `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/search-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautomate/latest/actions/search-contacts?${params}`, {
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
| `channel` | string | no |  |
| `locationId` | string | no |  |
| `searchText` | string | no |  |
| `tags` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "id": "string",
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "location": {},
      "name": "Ava Chen",
      "notes": "string",
      "phoneNumber": "string",
      "tags": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `createdAt` | date |  |
| `customFields` | object |  |
| `id` | string |  |
| `lastActivity` | date |  |
| `location` | object |  |
| `name` | string |  |
| `notes` | string |  |
| `phoneNumber` | string |  |
| `tags` | array<string> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Whautomate API, this operation is `GET /v1/contacts` (base URL `https://api.whautomate.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

