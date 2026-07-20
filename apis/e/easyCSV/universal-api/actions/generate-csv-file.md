# EasyCSV: Generate CSV File

Creates a CSV file in EasyCSV from JSON data.

```
POST https://connect.mindcloud.co/v1/universal/easyCSV/latest/actions/generate-csv-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyCSV `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `generatorId` | string | yes | The CSV Generator webhook token from the EasyCSV webhook URL. |
| `data` | string | yes | A JSON array of objects to turn into CSV rows. Send it as a stringified JSON array, matching the EasyCSV docs for the data parameter. |
| `recipientEmail` | string | no | Optional email address to send the generated CSV file to. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `temp_file_url` | string | Temporary public URL to the generated EasyCSV output file when temp-file access is enabled. |

## Native endpoint

Through the native EasyCSV API, this operation is `POST /generate_csv/:generatorId` (base URL `https://www.easycsv.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-csv-file.md) for the provider-specific parameters and requirements.

