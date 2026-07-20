# Billetweb: List Event Sessions

Retrieves sessions for a Billetweb event.

```
GET https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-event-sessions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billetweb `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-event-sessions?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-event-sessions?${params}`, {
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
| `id` | number | yes | Event identifier. |
| `past` | boolean | no | Include past sessions. |
| `lastUpdate` | number | no | Only return sessions updated after this Unix timestamp. |
| `disabled` | number | no | Filter by visibility state. |
| `pastBy` | number | no | Include sessions ended within the last X days. |
| `startFrom` | number | no | Filter from this session start Unix timestamp. |
| `startTo` | number | no | Filter until this session start Unix timestamp. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billetweb API returns.

## Native endpoint

Through the native Billetweb API, this operation is `GET /event/:id/dates` (base URL `https://www.billetweb.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-sessions.md) for the provider-specific parameters and requirements.

