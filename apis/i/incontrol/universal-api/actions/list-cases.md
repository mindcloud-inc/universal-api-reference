# Incontrol: List Cases

Retrieves a list of cases from Incontrol.

```
GET https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/list-cases
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Incontrol `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/list-cases?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/list-cases?${params}`, {
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
      "count": 1,
      "page": 1,
      "perPage": 1,
      "response": [
        {
          "created": "2026-05-07T12:00:00.000Z",
          "deadline": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "name": "Ava Chen",
          "number": 1,
          "organization": {},
          "priority": "string",
          "status": "string",
          "updated": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `page` | number |  |
| `perPage` | number |  |
| `response` | array<object> |  |
| `response[].created` | date |  |
| `response[].deadline` | date |  |
| `response[].id` | string |  |
| `response[].name` | string |  |
| `response[].number` | number |  |
| `response[].organization` | object |  |
| `response[].priority` | string |  |
| `response[].status` | string |  |
| `response[].updated` | date |  |

## Native endpoint

Through the native Incontrol API, this operation is `GET /api/v1/case` (base URL `https://portal.incontrol.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-cases.md) for the provider-specific parameters and requirements.

