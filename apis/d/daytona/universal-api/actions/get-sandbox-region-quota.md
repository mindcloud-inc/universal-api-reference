# Daytona: Get Sandbox Region Quota

Retrieves the sandbox region quota from Daytona.

```
GET https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-sandbox-region-quota
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Daytona `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-sandbox-region-quota?connectionId=$CONNECTION_ID&sandboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sandboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/daytona/latest/actions/get-sandbox-region-quota?${params}`, {
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
| `sandboxId` | string | yes | ID of the sandbox. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "organizationId": "string",
      "regionId": "string",
      "totalCpuQuota": 1,
      "totalDiskQuota": 1,
      "totalMemoryQuota": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `organizationId` | string | The organization ID. |
| `regionId` | string | The region ID. |
| `totalCpuQuota` | number | The total CPU quota. |
| `totalDiskQuota` | number | The total disk quota. |
| `totalMemoryQuota` | number | The total memory quota. |

## Native endpoint

Through the native Daytona API, this operation is `GET /sandbox/[:sandboxId]/region-quota` (base URL `https://app.daytona.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sandbox-region-quota.md) for the provider-specific parameters and requirements.

