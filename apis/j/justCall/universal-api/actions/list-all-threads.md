# JustCall: List All Threads

Retrieves text threads from JustCall.

```
GET https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-threads
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JustCall `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-threads?connectionId=$CONNECTION_ID&limit=25&offset=0&phoneId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "phoneId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-threads?${params}`, {
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
| `phoneId` | number | yes |  |
| `fromDateTime` | string | no |  |
| `toDateTime` | string | no |  |
| `contactNumber` | string | no |  |
| `keyword` | string | no |  |
| `tagId` | number | no |  |
| `order` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "currentPage": 1,
      "data": [
        {}
      ],
      "nextPageLink": "https://example.com",
      "perPage": 1,
      "prevPageLink": "https://example.com",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `currentPage` | number |  |
| `data` | array<object> |  |
| `nextPageLink` | string |  |
| `perPage` | number |  |
| `prevPageLink` | string |  |
| `totalCount` | number |  |

## Native endpoint

Through the native JustCall API, this operation is `GET /v2.1/texts/threads` (base URL `https://api.justcall.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-all-threads.md) for the provider-specific parameters and requirements.

