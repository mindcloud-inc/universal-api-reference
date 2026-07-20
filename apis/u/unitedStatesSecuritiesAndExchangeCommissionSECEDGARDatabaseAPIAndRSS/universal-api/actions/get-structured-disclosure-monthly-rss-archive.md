# United States Securities and Exchange Commission (SEC) EDGAR Database: Get Structured Disclosure Monthly RSS Archive

Retrieves a monthly structured disclosure RSS archive from SEC EDGAR.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-structured-disclosure-monthly-rss-archive
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-structured-disclosure-monthly-rss-archive?connectionId=$CONNECTION_ID&yearMonth=2026-03" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "yearMonth": "2026-03"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-structured-disclosure-monthly-rss-archive?${params}`, {
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
| `yearMonth` | string | yes | Structured disclosure monthly archive identifier in YYYY-MM format. Example: `2026-03`. |

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

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `GET /Archives/edgar/monthly/xbrlrss-[:yearMonth].xml` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-structured-disclosure-monthly-rss-archive.md) for the provider-specific parameters and requirements.

