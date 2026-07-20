# DataBridge: Get Folder

Retrieves a folder from DataBridge.

```
GET https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataBridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/get-folder?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/get-folder?${params}`, {
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
      "appId": {},
      "childCount": {},
      "depth": {},
      "description": {},
      "documentIds": {},
      "endUserId": {},
      "fullPath": {},
      "id": "string",
      "name": "Ava Chen",
      "parentId": {},
      "summaryBucket": {},
      "summaryStorageKey": {},
      "summaryUpdatedAt": {},
      "summaryVersion": {},
      "systemMetadata": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appId` | object |  |
| `childCount` | object |  |
| `depth` | object |  |
| `description` | object |  |
| `documentIds` | object |  |
| `endUserId` | object |  |
| `fullPath` | object |  |
| `id` | string |  |
| `name` | string |  |
| `parentId` | object |  |
| `summaryBucket` | object |  |
| `summaryStorageKey` | object |  |
| `summaryUpdatedAt` | object |  |
| `summaryVersion` | object |  |
| `systemMetadata` | object |  |

## Native endpoint

Through the native DataBridge API, this operation is `GET /folders/:folder_id_or_name` (base URL `https://api.morphik.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.

