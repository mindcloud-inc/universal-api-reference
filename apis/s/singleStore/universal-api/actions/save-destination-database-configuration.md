# SingleStore: Save Destination Database Configuration

Updates the destination database configuration in SingleStore.

```
PUT https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/save-destination-database-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SingleStore `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/save-destination-database-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "host": "string",
  "port": 1,
  "uid": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/save-destination-database-configuration', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "host": "string",
    "port": 1,
    "uid": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `host` | string | yes | Hostname or IP address of the destination database server. |
| `port` | number | yes | Port number for the destination database server. |
| `uid` | string | yes | Database username for the destination connection. |
| `type` | string | yes | SingleStore database type identifier for the destination connection, for example mysql. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SingleStore API returns.

## Native endpoint

Through the native SingleStore API, this operation is `PATCH /conn-dst` (base URL `https://{{credentials.flowEndpoint}}:30081/ingest/api/ingest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/save-destination-database-configuration.md) for the provider-specific parameters and requirements.

