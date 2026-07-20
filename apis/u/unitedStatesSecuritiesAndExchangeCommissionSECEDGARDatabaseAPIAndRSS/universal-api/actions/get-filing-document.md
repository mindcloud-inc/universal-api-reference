# United States Securities and Exchange Commission (SEC) EDGAR Database: Get Filing Document

Retrieves a filing document from the SEC EDGAR archive.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-filing-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-filing-document?connectionId=$CONNECTION_ID&cik=320193&accessionNumberNoDashes=000032019324000123&documentName=aapl-20240928.htm" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cik": "320193",
  "accessionNumberNoDashes": "000032019324000123",
  "documentName": "aapl-20240928.htm"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-filing-document?${params}`, {
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
| `cik` | string | yes | CIK directory segment, usually without leading zeroes in SEC archive paths. Example: `320193`. |
| `accessionNumberNoDashes` | string | yes | Accession number directory segment without dashes. Example: `000032019324000123`. |
| `documentName` | string | yes | Document file name inside the filing directory, such as aapl-20240928.htm. Example: `aapl-20240928.htm`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Raw response bytes returned by SEC. |
| `type` | string | Node Buffer marker for raw SEC response content. |

## Native endpoint

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `GET /Archives/edgar/data/[:cik]/[:accessionNumberNoDashes]/[:documentName]` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-filing-document.md) for the provider-specific parameters and requirements.

