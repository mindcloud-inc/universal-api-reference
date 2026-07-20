# Salesflare: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesflare `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-contacts?${params}`, {
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
| `limit` | number | no | Maximum number of contacts to return. |
| `offset` | number | no | Number of contacts to skip before returning results. |
| `orderBy` | string | no | Sort expression such as name or creation_date desc. |
| `search` | string | no | Free-text search across contacts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": {},
      "archived": true,
      "creationDate": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "email": "ava@example.com",
      "id": 1,
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "owner": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | object |  |
| `archived` | boolean |  |
| `creationDate` | date |  |
| `domain` | string |  |
| `email` | string |  |
| `id` | number |  |
| `modificationDate` | date |  |
| `name` | string |  |
| `owner` | object |  |

## Native endpoint

Through the native Salesflare API, this operation is `GET contacts` (base URL `https://api.salesflare.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

