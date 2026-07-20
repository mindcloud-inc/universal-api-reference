# EARLY: List Time Entries in Range

Retrieves time entries from EARLY in a date range.

```
GET https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/list-time-entries-in-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EARLY `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/list-time-entries-in-range?connectionId=$CONNECTION_ID&start=string&end=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "start": "string",
  "end": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eARLY/latest/actions/list-time-entries-in-range?${params}`, {
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
| `start` | string | yes | Range start timestamp in EARLY format, for example 2016-01-01T00:00:00.000. |
| `end` | string | yes | Range end timestamp in EARLY format, for example 2017-12-31T23:59:59.999. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native EARLY API returns.

## Native endpoint

Through the native EARLY API, this operation is `GET /api/v4/time-entries/:start/:end` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-time-entries-in-range.md) for the provider-specific parameters and requirements.

