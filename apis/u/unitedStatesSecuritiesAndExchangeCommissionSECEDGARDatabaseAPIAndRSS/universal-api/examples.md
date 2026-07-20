# United States Securities and Exchange Commission (SEC) EDGAR Database Universal API Examples

These examples use the MindCloud API key and United States Securities and Exchange Commission (SEC) EDGAR Database connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Company Tickers

Retrieves company ticker mappings from SEC EDGAR.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/list-company-tickers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/list-company-tickers?${params}`, {
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

See the full [List Company Tickers action reference](actions/list-company-tickers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/list-company-tickers).

## Create Custom CCC

Updates a filer's CCC to a custom value in EDGAR.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/create-custom-ccc" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cik": "0000320193",
  "ccc": "123456",
  "newCCC": "654321"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/create-custom-ccc', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cik": "0000320193",
    "ccc": "123456",
    "newCCC": "654321"
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
      "filerCCC": "string",
      "locator": "string",
      "messages": [
        {}
      ],
      "tracking": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Custom CCC action reference](actions/create-custom-ccc.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/create-custom-ccc).
