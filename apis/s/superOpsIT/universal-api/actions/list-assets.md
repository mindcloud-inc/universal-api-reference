# SuperOps IT: List Assets



```
GET https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-assets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-assets?${params}`, {
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
      "getAssetList": {
        "assets": [
          {
            "assetClass": {
              "classId": "string",
              "name": "Ava Chen"
            },
            "assetId": "string",
            "lastCommunicatedTime": "2026-05-07T12:00:00.000Z",
            "lastReportedTime": "2026-05-07T12:00:00.000Z",
            "manufacturer": "string",
            "model": "string",
            "name": "Ava Chen",
            "requester": {
              "email": "ava@example.com",
              "name": "Ava Chen"
            },
            "serialNumber": "string",
            "site": {
              "id": "string",
              "name": "Ava Chen"
            },
            "status": "string"
          }
        ],
        "listInfo": {
          "page": 1,
          "pageSize": 1,
          "totalCount": 1
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
| `getAssetList.assets[].assetClass.classId` | string |  |
| `getAssetList.assets[].assetClass.name` | string |  |
| `getAssetList.assets[].assetId` | string |  |
| `getAssetList.assets[].lastCommunicatedTime` | date |  |
| `getAssetList.assets[].lastReportedTime` | date |  |
| `getAssetList.assets[].manufacturer` | string |  |
| `getAssetList.assets[].model` | string |  |
| `getAssetList.assets[].name` | string |  |
| `getAssetList.assets[].requester.email` | string |  |
| `getAssetList.assets[].requester.name` | string |  |
| `getAssetList.assets[].serialNumber` | string |  |
| `getAssetList.assets[].site.id` | string |  |
| `getAssetList.assets[].site.name` | string |  |
| `getAssetList.assets[].status` | string |  |
| `getAssetList.listInfo.page` | number |  |
| `getAssetList.listInfo.pageSize` | number |  |
| `getAssetList.listInfo.totalCount` | number |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-assets.md) for the provider-specific parameters and requirements.

