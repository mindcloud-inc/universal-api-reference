# SuperOps IT: List Asset Software



```
GET https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-asset-software
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-asset-software?connectionId=$CONNECTION_ID&limit=25&offset=0&assetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "assetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/list-asset-software?${params}`, {
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
      "getAssetSoftwareList": {
        "assetSoftwares": [
          {
            "bitVersion": "string",
            "id": "string",
            "installedDate": "2026-05-07T12:00:00.000Z",
            "installedPath": "string",
            "software": {
              "manufacturer": "string",
              "name": "Ava Chen",
              "softwareId": "string"
            },
            "version": "string"
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
| `getAssetSoftwareList.assetSoftwares[].bitVersion` | string |  |
| `getAssetSoftwareList.assetSoftwares[].id` | string |  |
| `getAssetSoftwareList.assetSoftwares[].installedDate` | date |  |
| `getAssetSoftwareList.assetSoftwares[].installedPath` | string |  |
| `getAssetSoftwareList.assetSoftwares[].software.manufacturer` | string |  |
| `getAssetSoftwareList.assetSoftwares[].software.name` | string |  |
| `getAssetSoftwareList.assetSoftwares[].software.softwareId` | string |  |
| `getAssetSoftwareList.assetSoftwares[].version` | string |  |
| `getAssetSoftwareList.listInfo.page` | number |  |
| `getAssetSoftwareList.listInfo.pageSize` | number |  |
| `getAssetSoftwareList.listInfo.totalCount` | number |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-asset-software.md) for the provider-specific parameters and requirements.

