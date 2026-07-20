# SingleStore: Test Source Database Connection

Tests the source database connection in SingleStore.

```
GET https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/test-source-database-connection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SingleStore `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/test-source-database-connection?connectionId=$CONNECTION_ID&host=string&port=1&uid=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "host": "string",
  "port": "1",
  "uid": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/singleStore/latest/actions/test-source-database-connection?${params}`, {
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
| `host` | string | yes | Hostname or IP address of the source database server. |
| `port` | number | yes | Port number for the source database server. |
| `uid` | string | yes | Database username for the source connection. |
| `type` | string | yes | SingleStore database type identifier for the source connection, for example mysql. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messageList": [
        {
          "message": "string",
          "status": "string",
          "topic": "string"
        }
      ],
      "status": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageList[].message` | string | Error message for a failed test. |
| `messageList[].status` | string | Error severity status for a failed test. |
| `messageList[].topic` | string | Error topic for a failed test. |
| `status` | string | Provider status code returned on failure examples. |
| `success` | boolean | Whether the source connection test succeeded. |

## Native endpoint

Through the native SingleStore API, this operation is `POST /conn-src/test` (base URL `https://{{credentials.flowEndpoint}}:30081/ingest/api/ingest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/test-source-database-connection.md) for the provider-specific parameters and requirements.

