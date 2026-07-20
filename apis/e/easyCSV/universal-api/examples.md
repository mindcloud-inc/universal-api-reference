# EasyCSV Universal API Examples

These examples use the MindCloud API key and EasyCSV connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate CSV File

Creates a CSV file in EasyCSV from JSON data.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyCSV/latest/actions/generate-csv-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "generatorId": "string",
  "data": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyCSV/latest/actions/generate-csv-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "generatorId": "string",
    "data": "string"
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
      "temp_file_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Generate CSV File action reference](actions/generate-csv-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyCSV/latest/actions/generate-csv-file).
