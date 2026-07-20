# Morgen: List Events

Retrieves events from Morgen.

```
GET https://connect.mindcloud.co/v1/universal/morgen/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Morgen `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morgen/latest/actions/list-events?connectionId=$CONNECTION_ID&start=2026-03-20T00%3A00%3A00Z&end=2026-03-21T00%3A00%3A00Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "2026-03-20T00:00:00Z",
  "end": "2026-03-21T00:00:00Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morgen/latest/actions/list-events?${params}`, {
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
| `accountId` | string | no | Calendar account ID. Defaults to the connection accountId. Default: `{{credentials.accountId}}`. |
| `calendarIds` | string | no | Comma-separated calendar IDs. Defaults to the connection calendarId. Default: `{{credentials.calendarId}}`. |
| `start` | string | yes | Inclusive window start in ISO 8601 UTC format. Example: `2026-03-20T00:00:00Z`. |
| `end` | string | yes | Exclusive window end in ISO 8601 UTC format. Example: `2026-03-21T00:00:00Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Morgen API returns.

## Native endpoint

Through the native Morgen API, this operation is `GET /v3/events/list` (base URL `https://api.morgen.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

