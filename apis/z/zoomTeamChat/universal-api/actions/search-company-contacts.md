# Zoom Team Chat: Search Company Contacts



```
GET https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/search-company-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoom Team Chat `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/search-company-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&searchKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "searchKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zoomTeamChat/latest/actions/search-company-contacts?${params}`, {
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
| `searchKey` | string | yes | First name, last name, or email address of the contact to search for. |
| `queryPresenceStatus` | boolean | no | Whether to include the contact's presence status. |
| `contactTypes` | string | no | Comma-separated contact type codes. Default: `1`. |
| `userStatus` | string | no | User status such as active or inactive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "member_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `member_id` | string |  |

## Native endpoint

Through the native Zoom Team Chat API, this operation is `GET /contacts` (base URL `https://api.zoom.us/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-company-contacts.md) for the provider-specific parameters and requirements.

