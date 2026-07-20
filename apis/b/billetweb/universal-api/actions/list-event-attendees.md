# Billetweb: List Event Attendees

Retrieves attendees for a Billetweb event.

```
GET https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-event-attendees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billetweb `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-event-attendees?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-event-attendees?${params}`, {
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
| `lastUpdate` | number | no | Only return attendees updated after this Unix timestamp. |
| `since` | number | no | Only return attendees updated during the last N minutes. |
| `to` | number | no | Only return attendees modified before this Unix timestamp. |
| `session` | string | no | Filter by a specific session identifier. |
| `futurSessions` | boolean | no | Only include non-past sessions. |
| `used` | number | no | Filter by check-in state. |
| `ticket` | number | no | Filter by ticket identifier. |
| `email` | string | no | Filter by buyer email. |
| `extId` | string | no | Filter by external ticket identifier. |
| `barcode` | string | no | Filter by barcode. |
| `disabled` | number | no | Include refunded or canceled tickets. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billetweb API returns.

## Native endpoint

Through the native Billetweb API, this operation is `GET /event/:id/attendees` (base URL `https://www.billetweb.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-attendees.md) for the provider-specific parameters and requirements.

