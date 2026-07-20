# QStash: Add URL Group Endpoints

Adds endpoints to a QStash URL Group, creating it if needed.

```
POST https://connect.mindcloud.co/v1/universal/qStash/latest/actions/add-url-group-endpoints
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/add-url-group-endpoints" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urlGroupName": "https://example.com",
  "endpoints[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qStash/latest/actions/add-url-group-endpoints', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urlGroupName": "https://example.com",
    "endpoints[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urlGroupName` | string | yes | Name of the URL Group. |
| `endpoints[]` | array<object> | yes | Endpoints to add to the URL Group. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native QStash API returns.

## Native endpoint

Through the native QStash API, this operation is `POST /v2/topics/:urlGroupName/endpoints` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-url-group-endpoints.md) for the provider-specific parameters and requirements.

