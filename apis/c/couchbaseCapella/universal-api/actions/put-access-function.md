# Couchbase Capella: Upsert custom Access Control and Validation function

Upserts a custom access control and validation function in Couchbase Capella.

```
PUT https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/put-access-function
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Couchbase Capella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/put-access-function" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/put-access-function', {
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

Through the native Couchbase Capella API, this operation is `PUT /v4/organizations/:organizationId/projects/:projectId/clusters/:clusterId/appservices/:appServiceId/appEndpoints/:appEndpointKeyspace/accessControlFunction` (base URL `https://cloudapi.cloud.couchbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-access-function.md) for the provider-specific parameters and requirements.

