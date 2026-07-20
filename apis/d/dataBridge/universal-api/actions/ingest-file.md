# DataBridge: Ingest File

Creates a document in DataBridge from a file.

```
POST https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/ingest-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataBridge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/ingest-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dataBridge/latest/actions/ingest-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalMetadata": {},
      "appId": {},
      "chunkIds": [
        "string"
      ],
      "contentType": "string",
      "endUserId": {},
      "externalId": "string",
      "filename": {},
      "folderId": {},
      "folderName": {},
      "folderPath": {},
      "metadata": {},
      "metadataTypes": {},
      "storageInfo": {},
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
| `additionalMetadata` | object |  |
| `appId` | object |  |
| `chunkIds` | array<string> |  |
| `contentType` | string |  |
| `endUserId` | object |  |
| `externalId` | string |  |
| `filename` | object |  |
| `folderId` | object |  |
| `folderName` | object |  |
| `folderPath` | object |  |
| `metadata` | object |  |
| `metadataTypes` | object |  |
| `storageInfo` | object |  |
| `summaryBucket` | object |  |
| `summaryStorageKey` | object |  |
| `summaryUpdatedAt` | object |  |
| `summaryVersion` | object |  |
| `systemMetadata` | object |  |

## Native endpoint

Through the native DataBridge API, this operation is `POST /ingest/file` (base URL `https://api.morphik.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ingest-file.md) for the provider-specific parameters and requirements.

