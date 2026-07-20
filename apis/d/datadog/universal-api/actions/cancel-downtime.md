# Datadog: Cancel Downtime

Cancels an existing downtime in Datadog.

```
DELETE https://connect.mindcloud.co/v1/universal/datadog/latest/actions/cancel-downtime
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/cancel-downtime?connectionId=$CONNECTION_ID&downtimeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "downtimeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/cancel-downtime?${params}`, {
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
| `downtimeId` | string | yes | The ID of the downtime. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Datadog API returns.

## Native endpoint

Through the native Datadog API, this operation is `DELETE /api/v2/downtime/:downtime_id` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-downtime.md) for the provider-specific parameters and requirements.

