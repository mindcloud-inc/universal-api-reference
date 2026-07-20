# AntsRoute: Get Route by Agent and Date

Retrieves an AntsRoute route by agent and date.

```
GET https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/get-route-by-agent-and-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AntsRoute `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/get-route-by-agent-and-date?connectionId=$CONNECTION_ID&agentEmail=ava%40example.com&date=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentEmail": "ava@example.com",
  "date": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/antsRoute/latest/actions/get-route-by-agent-and-date?${params}`, {
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
| `date` | string | yes | format: yyyy-MM-dd |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AntsRoute API returns.

## Native endpoint

Through the native AntsRoute API, this operation is `GET /capi/route/:agentEmail/:date` (base URL `https://app.antsroute.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-route-by-agent-and-date.md) for the provider-specific parameters and requirements.

