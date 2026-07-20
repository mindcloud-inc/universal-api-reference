# Griptape: Stream Assistant Run Events

Streams assistant run events from Griptape.

```
GET https://connect.mindcloud.co/v1/universal/griptape/latest/actions/stream-assistant-run-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Griptape `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/griptape/latest/actions/stream-assistant-run-events?connectionId=$CONNECTION_ID&assistantRunId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assistantRunId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/griptape/latest/actions/stream-assistant-run-events?${params}`, {
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
| `assistantRunId` | string | yes | The assistant run ID whose events should be streamed. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Griptape API returns.

## Native endpoint

Through the native Griptape API, this operation is `GET /api/assistant-runs/:assistant_run_id/events/stream` (base URL `https://cloud.griptape.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stream-assistant-run-events.md) for the provider-specific parameters and requirements.

