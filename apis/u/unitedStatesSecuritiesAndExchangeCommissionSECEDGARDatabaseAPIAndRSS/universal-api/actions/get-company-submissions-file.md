# United States Securities and Exchange Commission (SEC) EDGAR Database: Get Company Submissions File

Retrieves a company submissions file from SEC EDGAR.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-submissions-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-submissions-file?connectionId=$CONNECTION_ID&fileName=CIK0000320193-submissions-001.json" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileName": "CIK0000320193-submissions-001.json"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-submissions-file?${params}`, {
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
| `fileName` | string | yes | Submissions file name returned in filings.files, such as CIK0000320193-submissions-001.json. Example: `CIK0000320193-submissions-001.json`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptanceDateTime": [
        "string"
      ],
      "accessionNumber": [
        "string"
      ],
      "act": [
        "string"
      ],
      "fileNumber": [
        "string"
      ],
      "filingDate": [
        "2026-05-07T12:00:00.000Z"
      ],
      "filmNumber": [
        "string"
      ],
      "form": [
        "string"
      ],
      "isInlineXBRL": [
        1
      ],
      "isXBRL": [
        1
      ],
      "items": [
        "string"
      ],
      "primaryDocDescription": [
        "string"
      ],
      "primaryDocument": [
        "string"
      ],
      "reportDate": [
        "2026-05-07T12:00:00.000Z"
      ],
      "size": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptanceDateTime` | array<string> | SEC acceptance timestamps. |
| `accessionNumber` | array<string> | Filing accession numbers. |
| `act` | array<string> | SEC act codes. |
| `fileNumber` | array<string> | SEC file numbers. |
| `filingDate` | array<date> | Filing dates. |
| `filmNumber` | array<string> | SEC film numbers. |
| `form` | array<string> | SEC form types. |
| `isInlineXBRL` | array<number> | SEC inline XBRL indicator values. |
| `isXBRL` | array<number> | SEC XBRL indicator values. |
| `items` | array<string> | Reported item codes. |
| `primaryDocDescription` | array<string> | Primary filing document descriptions. |
| `primaryDocument` | array<string> | Primary filing document names. |
| `reportDate` | array<date> | Report dates. |
| `size` | array<number> | Filing sizes in bytes. |

## Native endpoint

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `GET https://data.sec.gov/submissions/[:fileName]` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-submissions-file.md) for the provider-specific parameters and requirements.

