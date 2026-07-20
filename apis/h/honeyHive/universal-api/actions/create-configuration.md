# HoneyHive: Create Configuration

Creates a new configuration in HoneyHive.

```
POST https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/create-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HoneyHive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/create-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project": "string",
  "name": "Ava Chen",
  "provider": "string",
  "parameters": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/honeyHive/latest/actions/create-configuration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project": "string",
    "name": "Ava Chen",
    "provider": "string",
    "parameters": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project` | string | yes | Project name. |
| `name` | string | yes | Configuration name. |
| `provider` | string | yes | Configuration provider. |
| `parameters` | object | yes | Configuration parameters. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HoneyHive API returns.

## Native endpoint

Through the native HoneyHive API, this operation is `POST /configurations` (base URL `https://api.honeyhive.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-configuration.md) for the provider-specific parameters and requirements.

