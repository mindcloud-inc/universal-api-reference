# United States Securities and Exchange Commission (SEC) EDGAR Database: List Feed Directory

Retrieves the SEC EDGAR quarterly feed directory listing.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/list-feed-directory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/list-feed-directory?connectionId=$CONNECTION_ID&year=2026&quarter=QTR2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2026",
  "quarter": "QTR2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/list-feed-directory?${params}`, {
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
| `year` | string | yes | Four-digit year, such as 2026. Example: `2026`. |
| `quarter` | string | yes | SEC quarter directory, such as QTR1, QTR2, QTR3, or QTR4. Example: `QTR2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "directory": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `directory` | object | Directory listing metadata and items for a SEC Feed quarter folder. |

## Native endpoint

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `GET /Archives/edgar/Feed/[:year]/[:quarter]/index.json` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-feed-directory.md) for the provider-specific parameters and requirements.

