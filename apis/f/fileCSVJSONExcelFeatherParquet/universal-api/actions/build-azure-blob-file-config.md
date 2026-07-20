# File (CSV, JSON, Excel, Feather, Parquet): Build Azure Blob File Config

Creates an Azure Blob file source configuration.

```
POST https://connect.mindcloud.co/v1/universal/fileCSVJSONExcelFeatherParquet/latest/actions/build-azure-blob-file-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a File (CSV, JSON, Excel, Feather, Parquet) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fileCSVJSONExcelFeatherParquet/latest/actions/build-azure-blob-file-config" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fileCSVJSONExcelFeatherParquet/latest/actions/build-azure-blob-file-config', {
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
      "dockerImageTag": "string",
      "dockerRepository": "string",
      "documentationUrl": "https://example.com",
      "name": "Ava Chen",
      "releaseStage": "string",
      "sourceDefinitionId": "string",
      "sourceType": "string",
      "spec": {},
      "supportLevel": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dockerImageTag` | string |  |
| `dockerRepository` | string |  |
| `documentationUrl` | string |  |
| `name` | string |  |
| `releaseStage` | string |  |
| `sourceDefinitionId` | string |  |
| `sourceType` | string |  |
| `spec` | object |  |
| `supportLevel` | string |  |

## Native endpoint

Through the native File (CSV, JSON, Excel, Feather, Parquet) API, this operation is `GET /oss_registry.json` (base URL `https://connectors.airbyte.com/files/registries/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/build-azure-blob-file-config.md) for the provider-specific parameters and requirements.

