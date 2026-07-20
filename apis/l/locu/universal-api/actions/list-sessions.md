# Locu: List Sessions

Retrieves a paginated list of sessions from Locu.

```
GET https://connect.mindcloud.co/v1/universal/locu/latest/actions/list-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Locu `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/locu/latest/actions/list-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/locu/latest/actions/list-sessions?${params}`, {
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
| `orderBy` | string | no |  |
| `order` | string | no |  |
| `startAfter` | string | no |  |
| `startBefore` | string | no |  |
| `includeActivities` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "finishedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isManual": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `finishedAt` | date |  |
| `id` | string |  |
| `isManual` | boolean |  |

## Native endpoint

Through the native Locu API, this operation is `GET /sessions` (base URL `https://api.locu.app/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sessions.md) for the provider-specific parameters and requirements.

