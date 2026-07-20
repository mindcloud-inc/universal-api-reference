# LangChain: Update Session



```
PUT https://connect.mindcloud.co/v1/universal/langChain/latest/actions/update-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LangChain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/langChain/latest/actions/update-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/langChain/latest/actions/update-session', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sessionId` | string | yes | Session identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "default_dataset_id": "string",
      "description": "string",
      "end_time": "2026-05-07T12:00:00.000Z",
      "extra": {},
      "id": "string",
      "last_run_start_time_live": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "reference_dataset_id": "string",
      "start_time": "2026-05-07T12:00:00.000Z",
      "tenant_id": "string",
      "trace_tier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `default_dataset_id` | string | Optional default dataset UUID. |
| `description` | string | Session description. |
| `end_time` | date | Session end timestamp. |
| `extra` | object | Additional metadata. |
| `id` | string | Session UUID. |
| `last_run_start_time_live` | date | Latest live run start time. |
| `name` | string | Session name. |
| `reference_dataset_id` | string | Optional reference dataset UUID. |
| `start_time` | date | Session start timestamp. |
| `tenant_id` | string | Workspace UUID. |
| `trace_tier` | string | Trace retention tier. |

## Native endpoint

Through the native LangChain API, this operation is `PATCH /api/v1/sessions/:sessionId` (base URL `https://api.smith.langchain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-session.md) for the provider-specific parameters and requirements.

