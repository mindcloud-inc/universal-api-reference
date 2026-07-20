# Couchbase Capella: Delete Backup Schedule

Deletes a backup schedule from Couchbase Capella.

```
DELETE https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/delete-cloud-snapshot-backup-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Couchbase Capella `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/delete-cloud-snapshot-backup-schedule?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/couchbaseCapella/latest/actions/delete-cloud-snapshot-backup-schedule?${params}`, {
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

Through the native Couchbase Capella API, this operation is `DELETE /v4/organizations/:organizationId/projects/:projectId/clusters/:clusterId/cloudsnapshotbackupschedule` (base URL `https://cloudapi.cloud.couchbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-cloud-snapshot-backup-schedule.md) for the provider-specific parameters and requirements.

