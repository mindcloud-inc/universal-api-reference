# Pachca (Admin): Search Messages

Finds messages in the Pachca Admin API by search query.

```
GET https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/search-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/search-messages?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/search-messages?${params}`, {
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
| `active` | boolean | no | Filter by active chats. |
| `chatIds[]` | array<number> | no | Filter by chat ids. |
| `createdFrom` | date | no | Filter messages created on or after this timestamp. |
| `createdTo` | date | no | Filter messages created on or before this timestamp. |
| `cursor` | string | no | Pagination cursor from meta.paginate.next_page. |
| `limit` | number | no | Number of results to return. |
| `order` | string | no | Sort direction. |
| `query` | string | no | Full-text search string. |
| `userIds[]` | array<number> | no | Filter by author user ids. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "meta": {
        "paginate": {
          "nextPage": "string"
        },
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `meta.paginate.nextPage` | string |  |
| `meta.total` | number |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `GET /search/messages` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-messages.md) for the provider-specific parameters and requirements.

