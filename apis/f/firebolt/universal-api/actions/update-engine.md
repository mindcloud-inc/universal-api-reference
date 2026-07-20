# Firebolt: Update Engine

Updates an existing engine in Firebolt.

```
PUT https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/update-engine
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/update-engine" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engineHost": "01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io",
  "engineName": "mc_fb_lifecycle_20260422_engine",
  "setClause": "AUTO_STOP = 15"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/update-engine', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engineHost": "01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io",
    "engineName": "mc_fb_lifecycle_20260422_engine",
    "setClause": "AUTO_STOP = 15"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineHost` | string | yes | System engine host to execute the ALTER ENGINE statement against. Example: `01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io`. |
| `engineName` | string | yes | The Firebolt engine to alter. Example: `mc_fb_lifecycle_20260422_engine`. |
| `setClause` | string | yes | The ALTER ENGINE SET clause, for example AUTO_STOP = 15 or DEFAULT_DATABASE = my_database. Example: `AUTO_STOP = 15`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "monitorSql": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Firebolt async acceptance message. |
| `monitorSql` | string | SQL statement that can be used to check the async query status. |
| `token` | string | Firebolt async query token. |

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineHost` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-engine.md) for the provider-specific parameters and requirements.

