# WhautoChat: Search Contacts

Finds contacts in WhautoChat.

```
GET https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhautoChat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/search-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/whautoChat/latest/actions/search-contacts?${params}`, {
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
| `tags` | string | no | Filter by tags |
| `workspaceId` | string | no | Filter by workspace |
| `channel` | string | no | Filter by channel |
| `searchText` | string | no | Free text search |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": {},
      "id": "string",
      "name": "Ava Chen",
      "notes": "string",
      "phoneNumber": "string",
      "stage": "string",
      "tags": [
        "string"
      ],
      "workspace": {
        "id": "string",
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields` | object |  |
| `id` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phoneNumber` | string |  |
| `stage` | string |  |
| `tags` | array<string> |  |
| `workspace.id` | string |  |
| `workspace.title` | string |  |

## Native endpoint

Through the native WhautoChat API, this operation is `GET /v1/contacts` (base URL `https://api.whauto.chat`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

