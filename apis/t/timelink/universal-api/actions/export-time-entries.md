# Timelink: Export Time Entries

Exports time entries from the Timelink workspace.

```
GET https://connect.mindcloud.co/v1/universal/timelink/latest/actions/export-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timelink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelink/latest/actions/export-time-entries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelink/latest/actions/export-time-entries?${params}`, {
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
| `start` | string | no | Export start date. Example: `2026-03-31`. |
| `end` | string | no | Export end date. Example: `2026-03-31`. |
| `client_id` | string | no | Filter export to one client. Example: `01ABC...`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Timelink API returns.

## Native endpoint

Through the native Timelink API, this operation is `POST /timeEntries/export` (base URL `https://api.timelink.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-time-entries.md) for the provider-specific parameters and requirements.

