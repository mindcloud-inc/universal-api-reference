# <img src="https://images.mindcloud.co/apps/icons/easy-csv_1773766778448.png" alt="EasyCSV logo" width="28" height="28"> EasyCSV: Universal API

Upload CSV, XLSX, and Google Sheets data into EasyCSV workflows, trigger hosted imports, and generate CSV files from JSON via EasyCSV webhook endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/easyCSV/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.easycsv.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate CSV File](actions/generate-csv-file.md):

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

## Actions (2)

### Csv File

| Action | Method | Description |
| --- | --- | --- |
| [Generate CSV File](actions/generate-csv-file.md) | POST | Creates a CSV file in EasyCSV from JSON data. |

### Sheet Import

| Action | Method | Description |
| --- | --- | --- |
| [Import CSV File From URL](actions/import-csv-file-from-url.md) | POST | Imports a CSV file into EasyCSV from a public URL. |

