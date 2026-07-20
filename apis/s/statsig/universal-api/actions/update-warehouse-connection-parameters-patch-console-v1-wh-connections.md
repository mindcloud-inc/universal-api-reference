# Statsig: Update Warehouse Connection Parameters

Updates warehouse connection parameters in Statsig.

```
PUT https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-warehouse-connection-parameters-patch-console-v1-wh-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-warehouse-connection-parameters-patch-console-v1-wh-connections" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-warehouse-connection-parameters-patch-console-v1-wh-connections', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databricks` | object | no | Request body field. |
| `snowflake` | object | no | Request body field. |
| `bigquery` | object | no | Request body field. |
| `redshift` | object | no | Request body field. |
| `athena` | object | no | Request body field. |

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

Through the native Statsig API, this operation is `PATCH /console/v1/wh_connections` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-warehouse-connection-parameters-patch-console-v1-wh-connections.md) for the provider-specific parameters and requirements.

