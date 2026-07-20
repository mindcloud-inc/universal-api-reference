# Incontrol: List Drafts

Retrieves a list of drafts from Incontrol.

```
GET https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/list-drafts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Incontrol `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/list-drafts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/incontrol/latest/actions/list-drafts?${params}`, {
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
          "createdLocal": "2026-05-07T12:00:00.000Z",
          "form": {},
          "id": "string",
          "name": "Ava Chen",
          "reference": "string",
          "revision": true,
          "shared": "string",
          "user": {}
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
| `response[].createdLocal` | date |  |
| `response[].form` | object |  |
| `response[].id` | string |  |
| `response[].name` | string |  |
| `response[].reference` | string |  |
| `response[].revision` | boolean |  |
| `response[].shared` | string |  |
| `response[].user` | object |  |

## Native endpoint

Through the native Incontrol API, this operation is `GET /api/v1/draft` (base URL `https://portal.incontrol.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-drafts.md) for the provider-specific parameters and requirements.

