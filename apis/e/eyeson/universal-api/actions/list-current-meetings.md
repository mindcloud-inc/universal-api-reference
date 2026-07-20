# Eyeson: List Current Meetings



```
GET https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/list-current-meetings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eyeson `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/list-current-meetings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/list-current-meetings?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | 1-based result page to fetch. Eyeson returns up to 25 rooms per page. Example: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "guestToken": "string",
      "id": "string",
      "name": "Ava Chen",
      "ready": true,
      "shutdown": true,
      "startedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `guestToken` | string | Guest token for the room. Treat as sensitive and low-priority in UI. |
| `id` | string | Meeting room identifier. |
| `name` | string | Meeting room name. |
| `ready` | boolean | Whether the room is ready. |
| `shutdown` | boolean | Whether the room has shut down. |
| `startedAt` | date | Room start timestamp from Eyeson `started_at`. |

## Native endpoint

Through the native Eyeson API, this operation is `GET /rooms` (base URL `https://api.eyeson.team`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-current-meetings.md) for the provider-specific parameters and requirements.

