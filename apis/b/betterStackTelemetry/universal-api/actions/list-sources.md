# Better Stack Telemetry: List Sources

Retrieves telemetry sources from Better Stack Telemetry.

```
GET https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/list-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Telemetry `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/list-sources?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/betterStackTelemetry/latest/actions/list-sources?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Telemetry API returns.

## Native endpoint

Through the native Better Stack Telemetry API, this operation is `GET /api/v1/sources` (base URL `https://telemetry.betterstack.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sources.md) for the provider-specific parameters and requirements.

