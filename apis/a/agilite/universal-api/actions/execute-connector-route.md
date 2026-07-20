# Agilite: Execute Connector Route

Executes a connector route in Agilite by profile and route key.

```
POST https://connect.mindcloud.co/v1/universal/agilite/latest/actions/execute-connector-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Agilite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/agilite/latest/actions/execute-connector-route" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "profileKey": "string",
  "routeKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/agilite/latest/actions/execute-connector-route', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "profileKey": "string",
    "routeKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `profileKey` | string | yes | Unique Connector profile key. |
| `routeKey` | string | yes | Configured connector route key. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | no | Optional JSON body values used by the connector profile. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Agilite API returns.

## Native endpoint

Through the native Agilite API, this operation is `POST /connectors/execute` (base URL `https://api.agilite.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-connector-route.md) for the provider-specific parameters and requirements.

