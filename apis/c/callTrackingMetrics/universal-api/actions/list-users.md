# CallTrackingMetrics: List Users

Retrieves users for an account from CallTrackingMetrics.

```
GET https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallTrackingMetrics `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callTrackingMetrics/latest/actions/list-users?${params}`, {
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
| `email` | string | no | Filter users by email address. |
| `filter` | string | no | Filter users by status or scope. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPage": 1,
      "page": 1,
      "perPage": 1,
      "previousPage": 1,
      "totalEntries": 1,
      "totalPages": 1,
      "users": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPage` | number |  |
| `page` | number |  |
| `perPage` | number |  |
| `previousPage` | number |  |
| `totalEntries` | number |  |
| `totalPages` | number |  |
| `users[]` | array<object> |  |
| `users[].accountId` | number |  |
| `users[].email` | string |  |
| `users[].firstName` | string |  |
| `users[].id` | string |  |
| `users[].language` | string |  |
| `users[].lastName` | string |  |
| `users[].liveCalls[]` | array |  |
| `users[].role` | string |  |
| `users[].status` | string |  |
| `users[].uid` | number |  |
| `users[].url` | string |  |
| `users[].useFilterV2` | boolean |  |

## Native endpoint

Through the native CallTrackingMetrics API, this operation is `GET /accounts/:accountId/users.json` (base URL `https://api.calltrackingmetrics.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

