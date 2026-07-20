# United States Securities and Exchange Commission (SEC) EDGAR Database: Get Company Filings Atom Feed

Retrieves a company filings Atom feed from SEC EDGAR.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-filings-atom-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-filings-atom-feed?connectionId=$CONNECTION_ID&cikOrTicker=AAPL" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "cikOrTicker": "AAPL"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-company-filings-atom-feed?${params}`, {
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
| `cikOrTicker` | string | yes | Company CIK or ticker symbol. Example: `AAPL`. |
| `formType` | string | no | Optional SEC form type filter, such as 10-K, 10-Q, or 8-K. Example: `10-K`. |
| `count` | number | no | Maximum number of feed entries returned by SEC browse search. Default: `40`. Example: `40`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `owner` | string | no | Ownership filing mode, such as exclude or include. Default: `exclude`. Example: `exclude`. |

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

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `GET /cgi-bin/browse-edgar` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-filings-atom-feed.md) for the provider-specific parameters and requirements.

