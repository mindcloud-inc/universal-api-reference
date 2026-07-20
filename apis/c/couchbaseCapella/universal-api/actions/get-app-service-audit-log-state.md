# Couchbase Capella: Get App Service Audit Log State

Retrieves an app service audit log state from Couchbase Capella.

```
GET https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/get-app-service-audit-log-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Couchbase Capella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/get-app-service-audit-log-state?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/get-app-service-audit-log-state?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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

Through the native Couchbase Capella API, this operation is `GET /v4/organizations/:organizationId/projects/:projectId/clusters/:clusterId/appservices/:appServiceId/auditLog` (base URL `https://cloudapi.cloud.couchbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-app-service-audit-log-state.md) for the provider-specific parameters and requirements.

