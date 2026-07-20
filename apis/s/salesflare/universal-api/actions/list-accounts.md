# Salesflare: List Accounts



```
GET https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesflare `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/list-accounts?${params}`, {
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
| `limit` | number | no | Maximum number of accounts to return. |
| `orderBy` | string | no | Sort expression such as name or creation_date desc. |
| `search` | string | no | Free-text search across accounts. |
| `offset` | number | no | Number of accounts to skip before returning results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationDate": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "id": 1,
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "owner": {},
      "picture": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationDate` | date |  |
| `domain` | string |  |
| `id` | number |  |
| `modificationDate` | date |  |
| `name` | string |  |
| `owner` | object |  |
| `picture` | string |  |
| `website` | string |  |

## Native endpoint

Through the native Salesflare API, this operation is `GET accounts` (base URL `https://api.salesflare.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

