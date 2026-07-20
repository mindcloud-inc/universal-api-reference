# Intradesk: List Knowledge Base Articles

Retrieves knowledge base articles from Intradesk.

```
GET https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-knowledge-base-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intradesk `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-knowledge-base-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intradesk/latest/actions/list-knowledge-base-articles?${params}`, {
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
      "createdat": "2026-05-07T12:00:00.000Z",
      "createdby": "string",
      "createdid": 1,
      "description": "string",
      "files": "string",
      "id": 1,
      "name": "Ava Chen",
      "servicepath": [
        {}
      ],
      "services": [
        {}
      ],
      "updatedat": "2026-05-07T12:00:00.000Z",
      "updatedby": "string",
      "updatedid": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdat` | date |  |
| `createdby` | string |  |
| `createdid` | number |  |
| `description` | string |  |
| `files` | string |  |
| `id` | number |  |
| `name` | string |  |
| `servicepath` | array<object> |  |
| `services` | array<object> |  |
| `updatedat` | date |  |
| `updatedby` | string |  |
| `updatedid` | number |  |

## Native endpoint

Through the native Intradesk API, this operation is `GET /knowledgebase/odata/v1/Kb` (base URL `https://apigw.intradesk.ru`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-knowledge-base-articles.md) for the provider-specific parameters and requirements.

