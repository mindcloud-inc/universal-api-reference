# Statsig: Create Ingestion Databricks

Creates a Databricks ingestion in Statsig.

```
POST https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-ingestion-databricks-post-console-v1-ingestion-connection-databricks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-ingestion-databricks-post-console-v1-ingestion-connection-databricks" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "token": "string",
  "host": "string",
  "path": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/create-ingestion-databricks-post-console-v1-ingestion-connection-databricks', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "token": "string",
    "host": "string",
    "path": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `token` | string | yes | Request body field. |
| `host` | string | yes | Request body field. |
| `path` | string | yes | Request body field. |
| `deltaSharingCredentials` | string | no | Request body field. |
| `verified` | boolean | no | Request body field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `POST /console/v1/ingestion/connection/databricks` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ingestion-databricks-post-console-v1-ingestion-connection-databricks.md) for the provider-specific parameters and requirements.

