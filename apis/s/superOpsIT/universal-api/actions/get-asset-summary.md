# SuperOps IT: Get Asset Summary



```
GET https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-asset-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-asset-summary?connectionId=$CONNECTION_ID&assetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-asset-summary?${params}`, {
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
| `assetId` | string | yes | The SuperOps asset ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "getAssetSummary": {
        "cpu": {
          "assetId": "string",
          "cpuName": "Ava Chen",
          "cpuUsage": 1,
          "currentSpeed": 1,
          "logicalCore": 1,
          "maxSpeed": 1,
          "physicalCore": 1
        },
        "disk": {
          "totalFreeSpace": 1,
          "totalSize": 1
        },
        "lastUserLog": {
          "id": "string",
          "lastLoginTime": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen"
        },
        "memory": {
          "availableMemory": 1,
          "memoryUsage": 1,
          "totalMemory": 1,
          "usedMemory": 1
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `getAssetSummary.cpu.assetId` | string |  |
| `getAssetSummary.cpu.cpuName` | string |  |
| `getAssetSummary.cpu.cpuUsage` | number |  |
| `getAssetSummary.cpu.currentSpeed` | number |  |
| `getAssetSummary.cpu.logicalCore` | number |  |
| `getAssetSummary.cpu.maxSpeed` | number |  |
| `getAssetSummary.cpu.physicalCore` | number |  |
| `getAssetSummary.disk.totalFreeSpace` | number |  |
| `getAssetSummary.disk.totalSize` | number |  |
| `getAssetSummary.lastUserLog.id` | string |  |
| `getAssetSummary.lastUserLog.lastLoginTime` | date |  |
| `getAssetSummary.lastUserLog.name` | string |  |
| `getAssetSummary.memory.availableMemory` | number |  |
| `getAssetSummary.memory.memoryUsage` | number |  |
| `getAssetSummary.memory.totalMemory` | number |  |
| `getAssetSummary.memory.usedMemory` | number |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset-summary.md) for the provider-specific parameters and requirements.

