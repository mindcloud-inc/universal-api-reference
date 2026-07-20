# AntsRoute: Get Agent Last Known Position

Retrieves an agent's last known position in AntsRoute.

```
GET https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/get-agent-last-known-position
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AntsRoute `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/get-agent-last-known-position?connectionId=$CONNECTION_ID&agentEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentEmail": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/get-agent-last-known-position?${params}`, {
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
| `agentEmail` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AntsRoute API returns.

## Native endpoint

Through the native AntsRoute API, this operation is `GET /capi/agent/:agentEmail/last-known-position` (base URL `https://app.antsroute.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-agent-last-known-position.md) for the provider-specific parameters and requirements.

