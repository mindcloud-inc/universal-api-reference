# Cakemail: Show Email Activity Logs

Retrieves email activity logs from Cakemail.

```
GET https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/show-email-activity-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cakemail `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/show-email-activity-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&logType=sent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "logType": "sent"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cakemail/latest/actions/show-email-activity-logs?${params}`, {
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
| `logType` | string | yes | Email log type to retrieve. Use sent, bounce, clickthru, open, unsubscribe, resubscribe, spam, global_unsubscribe, or all. Cakemail currently returns an upstream 500 for all on this tenant; sent is the safe default. Default: `sent`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cakemail API returns.

## Native endpoint

Through the native Cakemail API, this operation is `GET /logs/emails` (base URL `https://api.cakemail.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/show-email-activity-logs.md) for the provider-specific parameters and requirements.

