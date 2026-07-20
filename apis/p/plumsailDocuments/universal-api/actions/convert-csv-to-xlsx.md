# Plumsail Documents: Convert CSV to XLSX

Converts CSV to XLSX in Plumsail Documents.

```
POST https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/convert-csv-to-xlsx
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plumsail Documents `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/convert-csv-to-xlsx" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/plumsailDocuments/latest/actions/convert-csv-to-xlsx', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `hasHeaderRecords` | boolean | no | Whether the CSV includes a header row. |
| `delimiter` | string | no | Delimiter character used in the CSV file. |
| `locale` | string | no | Locale used when parsing CSV values. |
| `limit` | number | no | Maximum number of CSV rows to convert. |
| `mappings` | string | no | JSON mapping rules for CSV columns and output fields. |
| `file` | file | no | CSV file to upload. |
| `fileUrl` | string | no | Anonymous URL to a CSV file. |
| `callbackUrl` | string | no | Webhook URL to receive async completion notifications. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "link": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `link` | string |  |

## Native endpoint

Through the native Plumsail Documents API, this operation is `POST /api/v2/convert/csv-to-xlsx` (base URL `https://us-api.plumsail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-csv-to-xlsx.md) for the provider-specific parameters and requirements.

