# Firebolt: Create Database

Creates a new database in Firebolt.

```
POST https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/create-database
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Firebolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/create-database" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "engineUrl": "01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io",
  "databaseName": "mc_stage3_20260422_db1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebolt/latest/actions/create-database', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "engineUrl": "01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io",
    "databaseName": "mc_stage3_20260422_db1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `engineUrl` | string | yes | System engine host, for example 01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io. Example: `01kjtg5w4vwy72rfew4r8vg135.api.us-east-1.app.firebolt.io`. |
| `databaseName` | string | yes | Name of the Firebolt database to create. Example: `mc_stage3_20260422_db1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional database description, up to 64 characters. Example: `MindCloud stage 3 database`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Firebolt API returns.

## Native endpoint

Through the native Firebolt API, this operation is `POST https://:engineUrl` (base URL `https://api.app.firebolt.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-database.md) for the provider-specific parameters and requirements.

