# Billetweb: List All Attendees

Retrieves attendees across all Billetweb events.

```
GET https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-all-attendees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billetweb `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-all-attendees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billetweb/latest/actions/list-all-attendees?${params}`, {
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
| `lastUpdate` | number | no | Only return attendees updated after this Unix timestamp. |
| `since` | number | no | Only return attendees updated during the last N minutes. |
| `to` | number | no | Only return attendees modified before this Unix timestamp. |
| `tag` | string | no | Filter attendees for events containing a specific tag. |
| `futur` | boolean | no | Only include unfinished events. |
| `email` | string | no | Filter by buyer email. |
| `ticket` | number | no | Filter by ticket identifier. |
| `session` | string | no | Filter by session identifier. |
| `used` | number | no | Filter by check-in state. |
| `disabled` | number | no | Include refunded or canceled tickets. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Billetweb API returns.

## Native endpoint

Through the native Billetweb API, this operation is `GET /attendees` (base URL `https://www.billetweb.fr/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-attendees.md) for the provider-specific parameters and requirements.

