# Couchbase Capella: Get CLI Commands For Setting Up Private Endpoint Connection

Retrieves CLI commands for a private endpoint connection from Couchbase Capella.

```
POST https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/get-data-api-private-endpoint-command
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Couchbase Capella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/get-data-api-private-endpoint-command" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/get-data-api-private-endpoint-command', {
  method: 'POST',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Operation result. |

## Native endpoint

Through the native Couchbase Capella API, this operation is `POST /v4/organizations/:organizationId/projects/:projectId/clusters/:clusterId/dataAPI/privateEndpointCommand` (base URL `https://cloudapi.cloud.couchbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-api-private-endpoint-command.md) for the provider-specific parameters and requirements.

