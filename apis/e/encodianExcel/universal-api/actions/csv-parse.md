# Encodian - Excel: CSV - Parse

Parses a CSV file into JSON in Encodian - Excel.

```
GET https://connect.mindcloud.co/v1/universal/encodianExcel/latest/actions/csv-parse
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Encodian - Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/encodianExcel/latest/actions/csv-parse?connectionId=$CONNECTION_ID&fileContent=bmFtZSxhbW91bnQKQWxpY2UsMTAKQm9iLDIwCg%3D%3D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileContent": "bmFtZSxhbW91bnQKQWxpY2UsMTAKQm9iLDIwCg=="
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/encodianExcel/latest/actions/csv-parse?${params}`, {
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
| `fileContent` | file | yes | The file content of the source CSV file. Default: `bmFtZSxhbW91bnQKQWxpY2UsMTAKQm9iLDIwCg==`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `delimiter` | string | no | Set the CSV delimiter. Defaults to comma. Default: `,`. |
| `encoding` | list<string> | no | One of: `ASCII`, `ISO88591`, `ISO88592`, `Latin1`, `UTF8`. Default: `UTF8`. |
| `csvColumnHeaders` | string | no | Optional comma-delimited column headers. |
| `skipFirstLine` | boolean | no | Skip the first line when the CSV contains headers. Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "csvData": "string",
      "Errors": [
        "string"
      ],
      "HttpStatusCode": 1,
      "HttpStatusMessage": "string",
      "OperationId": "string",
      "OperationStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `csvData` | string | Parsed CSV data in JSON format. |
| `Errors` | array<string> | Errors returned by Encodian. |
| `HttpStatusCode` | number | HTTP status code returned by Encodian. |
| `HttpStatusMessage` | string | HTTP status message returned by Encodian. |
| `OperationId` | string | Unique Encodian operation ID. |
| `OperationStatus` | string | Encodian operation status. |

## Native endpoint

Through the native Encodian - Excel API, this operation is `POST /api/v1/Excel/ParseCsv` (base URL `https://api.apps-encodian.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/csv-parse.md) for the provider-specific parameters and requirements.

