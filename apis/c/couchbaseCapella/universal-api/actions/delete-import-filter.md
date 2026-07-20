# Couchbase Capella: Delete Import Filter

Deletes an import filter from Couchbase Capella.

```
DELETE https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/delete-import-filter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Couchbase Capella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/delete-import-filter?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/delete-import-filter?${params}`, {
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

Through the native Couchbase Capella API, this operation is `DELETE /v4/organizations/:organizationId/projects/:projectId/clusters/:clusterId/appservices/:appServiceId/appEndpoints/:appEndpointKeyspace/importFilter` (base URL `https://cloudapi.cloud.couchbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-import-filter.md) for the provider-specific parameters and requirements.

