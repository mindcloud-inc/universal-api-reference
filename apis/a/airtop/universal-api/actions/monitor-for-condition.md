# Airtop: Monitor For Condition

Monitors an Airtop window for a condition.

```
GET https://connect.mindcloud.co/v1/universal/airtop/latest/actions/monitor-for-condition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airtop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airtop/latest/actions/monitor-for-condition?connectionId=$CONNECTION_ID&sessionId=string&windowId=string&condition=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sessionId": "string",
  "windowId": "string",
  "condition": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airtop/latest/actions/monitor-for-condition?${params}`, {
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
| `sessionId` | string | yes |  |
| `windowId` | string | yes |  |
| `condition` | string | yes | A natural language description of the condition to monitor for |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Airtop API returns.

## Native endpoint

Through the native Airtop API, this operation is `POST /sessions/:sessionId/windows/:windowId/monitor` (base URL `https://api.airtop.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/monitor-for-condition.md) for the provider-specific parameters and requirements.

