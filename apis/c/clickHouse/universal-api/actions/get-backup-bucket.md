# ClickHouse: Get Backup Bucket



```
GET https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-backup-bucket
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickHouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-backup-bucket?connectionId=$CONNECTION_ID&organizationId=string&serviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string",
  "serviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-backup-bucket?${params}`, {
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
| `organizationId` | string | yes | ID of the organization that owns the service. |
| `serviceId` | string | yes | ID of the requested service. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessKeyId": "string",
      "bucketPath": "string",
      "bucketProvider": "string",
      "containerName": "Ava Chen",
      "iamRoleArn": "string",
      "iamRoleSessionName": "Ava Chen",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessKeyId` | string | GCP HMAC access key ID for GCP backup buckets. |
| `bucketPath` | string | Backup bucket path. |
| `bucketProvider` | string | Backup bucket provider. |
| `containerName` | string | Azure container name for Azure backup buckets. |
| `iamRoleArn` | string | AWS IAM role ARN for AWS backup buckets. |
| `iamRoleSessionName` | string | AWS role session name for AWS backup buckets. |
| `id` | string | Unique backup bucket ID. |

## Native endpoint

Through the native ClickHouse API, this operation is `GET /v1/organizations/[:organizationId]/services/[:serviceId]/backupBucket` (base URL `https://api.clickhouse.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-backup-bucket.md) for the provider-specific parameters and requirements.

