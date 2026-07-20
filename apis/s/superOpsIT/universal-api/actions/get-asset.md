# SuperOps IT: Get Asset



```
GET https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperOps IT `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-asset?connectionId=$CONNECTION_ID&assetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superOpsIT/latest/actions/get-asset?${params}`, {
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
      "getAsset": {
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
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `getAsset.assetClass.classId` | string |  |
| `getAsset.assetClass.name` | string |  |
| `getAsset.assetId` | string |  |
| `getAsset.lastCommunicatedTime` | date |  |
| `getAsset.lastReportedTime` | date |  |
| `getAsset.manufacturer` | string |  |
| `getAsset.model` | string |  |
| `getAsset.name` | string |  |
| `getAsset.requester.email` | string |  |
| `getAsset.requester.name` | string |  |
| `getAsset.serialNumber` | string |  |
| `getAsset.site.id` | string |  |
| `getAsset.site.name` | string |  |
| `getAsset.status` | string |  |

## Native endpoint

Through the native SuperOps IT API, this operation is `POST /it` (base URL `https://api.superops.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset.md) for the provider-specific parameters and requirements.

