# Beyond Presence: List Calls

Retrieves agent-managed calls from Beyond Presence.

```
GET https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/list-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beyond Presence `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/list-calls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/list-calls?${params}`, {
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
      "agentId": "string",
      "endedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "tags": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string | ID of the agent managing the call. |
| `endedAt` | date | Call end time in ISO 8601 format when available. |
| `id` | string | Unique identifier of the call. |
| `startedAt` | date | Call start time in ISO 8601 format. |
| `tags` | object | Tags attached to the call. |

## Native endpoint

Through the native Beyond Presence API, this operation is `GET /v1/calls` (base URL `https://api.bey.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calls.md) for the provider-specific parameters and requirements.

