# Switchy.io: List UTM Templates

Retrieves UTM templates from Switchy.io.

```
GET https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/list-utm-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Switchy.io `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/list-utm-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/switchyio/latest/actions/list-utm-templates?${params}`, {
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
      "campaign": "string",
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "medium": "string",
      "name": "Ava Chen",
      "source": "string",
      "term": "string",
      "workspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | string |  |
| `content` | string |  |
| `createdAt` | date |  |
| `id` | number |  |
| `medium` | string |  |
| `name` | string |  |
| `source` | string |  |
| `term` | string |  |
| `workspaceId` | number |  |

## Native endpoint

Through the native Switchy.io API, this operation is `POST /v1/graphql` (base URL `https://graphql.switchy.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-utm-templates.md) for the provider-specific parameters and requirements.

