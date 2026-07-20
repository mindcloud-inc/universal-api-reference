# SuperOps IT: Update Asset



```
PUT https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/update-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/update-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/update-asset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assetId` | string | yes | The SuperOps asset ID to update. |
| `name` | string | no | Optional new asset name. |
| `siteId` | string | no | Optional site ID for the asset. |
| `requesterUserId` | string | no | Optional requester user ID. |
| `purchasedDate` | date | no | Optional purchased date in YYYY-MM-DD format. |
| `warrantyExpiryDate` | date | no | Optional warranty expiry date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "updateAsset": {
        "assetClass": {
          "classId": "string",
          "name": "Ava Chen"
        },
        "assetId": "string",
        "department": {
          "name": "Ava Chen"
        },
        "name": "Ava Chen",
        "requester": {
          "email": "ava@example.com",
          "name": "Ava Chen"
        },
        "site": {
          "id": "string",
          "name": "Ava Chen"
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
| `updateAsset.assetClass.classId` | string |  |
| `updateAsset.assetClass.name` | string |  |
| `updateAsset.assetId` | string |  |
| `updateAsset.department.name` | string |  |
| `updateAsset.name` | string |  |
| `updateAsset.requester.email` | string |  |
| `updateAsset.requester.name` | string |  |
| `updateAsset.site.id` | string |  |
| `updateAsset.site.name` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-asset.md) for the provider-specific parameters and requirements.

