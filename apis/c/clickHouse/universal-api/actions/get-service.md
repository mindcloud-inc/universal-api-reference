# ClickHouse: Get Service



```
GET https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickHouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-service?connectionId=$CONNECTION_ID&organizationId=string&serviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string",
  "serviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-service?${params}`, {
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
      "clickhouseVersion": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dataWarehouseId": "string",
      "endpoints": [
        {}
      ],
      "id": "string",
      "idleScaling": true,
      "idleTimeoutMinutes": 1,
      "ipAccessList": [
        {}
      ],
      "isPrimary": true,
      "isReadonly": true,
      "maxReplicaMemoryGb": 1,
      "mcpEnabled": true,
      "minReplicaMemoryGb": 1,
      "name": "Ava Chen",
      "numReplicas": 1,
      "provider": "string",
      "region": "string",
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clickhouseVersion` | string | ClickHouse version. |
| `createdAt` | date | Service creation timestamp. |
| `dataWarehouseId` | string | Data warehouse ID. |
| `endpoints` | array<object> | Connection endpoints for the service. |
| `id` | string | ClickHouse service ID. |
| `idleScaling` | boolean | Whether idle scaling is enabled. |
| `idleTimeoutMinutes` | number | Idle timeout in minutes. |
| `ipAccessList` | array<object> | IP access list entries. |
| `isPrimary` | boolean | Whether this is the primary service. |
| `isReadonly` | boolean | Whether the service is read-only. |
| `maxReplicaMemoryGb` | number | Maximum memory per replica in GiB. |
| `mcpEnabled` | boolean | Whether MCP is enabled for the service. |
| `minReplicaMemoryGb` | number | Minimum memory per replica in GiB. |
| `name` | string | Service name. |
| `numReplicas` | number | Replica count. |
| `provider` | string | Cloud provider. |
| `region` | string | Cloud region. |
| `state` | string | Current service state. |

## Native endpoint

Through the native ClickHouse API, this operation is `GET /v1/organizations/[:organizationId]/services/[:serviceId]` (base URL `https://api.clickhouse.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service.md) for the provider-specific parameters and requirements.

