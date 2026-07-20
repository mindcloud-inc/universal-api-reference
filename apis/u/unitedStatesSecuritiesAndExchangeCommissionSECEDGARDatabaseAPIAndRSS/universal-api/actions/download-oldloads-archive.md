# United States Securities and Exchange Commission (SEC) EDGAR Database: Download Oldloads Archive

Downloads a daily SEC EDGAR oldloads archive.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/download-oldloads-archive
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/download-oldloads-archive?connectionId=$CONNECTION_ID&year=2026&quarter=QTR2&loadDate=20260410" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "year": "2026",
  "quarter": "QTR2",
  "loadDate": "20260410"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/download-oldloads-archive?${params}`, {
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
| `loadDate` | string | yes | Oldloads archive date in YYYYMMDD format. Example: `20260410`. |

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

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `GET /Archives/edgar/Oldloads/[:year]/[:quarter]/[:loadDate].gz` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-oldloads-archive.md) for the provider-specific parameters and requirements.

