# File (CSV, JSON, Excel, Feather, Parquet) Universal API Examples

These examples use the MindCloud API key and File (CSV, JSON, Excel, Feather, Parquet) connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get File Connector Metadata

Retrieves metadata for the File source connector.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fileCSVJSONExcelFeatherParquet/latest/actions/get-file-connector-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fileCSVJSONExcelFeatherParquet/latest/actions/get-file-connector-metadata?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Get File Connector Metadata action reference](actions/get-file-connector-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fileCSVJSONExcelFeatherParquet/latest/actions/get-file-connector-metadata).

## Build Azure Blob File Config

Creates an Azure Blob file source configuration.

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

Example response:

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

See the full [Build Azure Blob File Config action reference](actions/build-azure-blob-file-config.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fileCSVJSONExcelFeatherParquet/latest/actions/build-azure-blob-file-config).
