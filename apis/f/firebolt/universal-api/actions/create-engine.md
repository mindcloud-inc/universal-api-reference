# Firebolt: Create Engine

Creates a new engine in Firebolt.

```
POST https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/create-engine
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/create-engine" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engineUrl": "01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io",
  "engineName": "mc_stage3_20260422_engine1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/create-engine', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engineUrl": "01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io",
    "engineName": "mc_stage3_20260422_engine1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineUrl` | string | yes | System engine host, for example 01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io. Example: `01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io`. |
| `engineName` | string | yes | Name of the Firebolt engine to create. Example: `mc_stage3_20260422_engine1`. |
| `defaultDatabase` | string | no | Optional default database for the new engine. Example: `mc_stage3_20260422_db1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `initiallyStopped` | boolean | no | When true, the new engine is created without starting immediately. |
| `autoStopMinutes` | number | no | Optional idle time in minutes before the engine auto-stops. Example: `5`. |
| `engineType` | string | no | Optional engine type such as S or M. Example: `S`. |
| `nodes` | number | no | Optional number of nodes per cluster. Example: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Firebolt API returns.

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineUrl` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-engine.md) for the provider-specific parameters and requirements.

