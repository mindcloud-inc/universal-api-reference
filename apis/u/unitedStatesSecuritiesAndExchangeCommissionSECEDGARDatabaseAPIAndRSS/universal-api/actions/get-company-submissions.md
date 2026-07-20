# United States Securities and Exchange Commission (SEC) EDGAR Database: Get Company Submissions

Retrieves company submission history from SEC EDGAR.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-submissions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-submissions?connectionId=$CONNECTION_ID&cik=0000320193" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cik": "0000320193"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-submissions?${params}`, {
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
| `cik` | string | yes | Zero-padded 10-digit Central Index Key, such as 0000320193 for Apple. Example: `0000320193`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": {},
      "category": "string",
      "cik": "string",
      "ein": "string",
      "entityType": "string",
      "exchanges": [
        "string"
      ],
      "files": [
        {}
      ],
      "filings": {},
      "fiscalYearEnd": "string",
      "formerNames": [
        {}
      ],
      "name": "Ava Chen",
      "phone": "string",
      "sic": "string",
      "sicDescription": "string",
      "stateOfIncorporation": "string",
      "tickers": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | object | Business and mailing address object. |
| `category` | string | SEC filer category. |
| `cik` | string | Central Index Key for the registrant. |
| `ein` | string | Employer Identification Number. |
| `entityType` | string | SEC entity type. |
| `exchanges` | array<string> | Known exchanges. |
| `files` | array<object> | Additional submissions files for the registrant. |
| `filings` | object | Recent filing arrays and older filing file references. |
| `fiscalYearEnd` | string | Fiscal year-end MMDD value. |
| `formerNames` | array<object> | Former registrant names. |
| `name` | string | Registrant name. |
| `phone` | string | Registrant phone number. |
| `sic` | string | Standard Industrial Classification code. |
| `sicDescription` | string | Description for the SIC code. |
| `stateOfIncorporation` | string | State of incorporation. |
| `tickers` | array<string> | Known public tickers. |

## Native endpoint

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `GET https://data.sec.gov/submissions/CIK[:cik].json` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-submissions.md) for the provider-specific parameters and requirements.

