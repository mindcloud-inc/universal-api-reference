# United States Securities and Exchange Commission (SEC) EDGAR Database: Get XBRL Frame

Retrieves XBRL frame data from SEC EDGAR.

```
GET https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-xbrl-frame
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a United States Securities and Exchange Commission (SEC) EDGAR Database `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-xbrl-frame?connectionId=$CONNECTION_ID&taxonomy=us-gaap&tag=AccountsPayableCurrent&unit=USD&period=CY2024" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taxonomy": "us-gaap",
  "tag": "AccountsPayableCurrent",
  "unit": "USD",
  "period": "CY2024"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unitedStatesSecuritiesAndExchangeCommissionSECEDGARDatabaseAPIAndRSS/latest/actions/get-xbrl-frame?${params}`, {
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
| `taxonomy` | string | yes | Taxonomy namespace, such as us-gaap, ifrs-full, dei, or srt. Example: `us-gaap`. |
| `tag` | string | yes | Taxonomy tag, such as AccountsPayableCurrent. Example: `AccountsPayableCurrent`. |
| `unit` | string | yes | XBRL unit, such as USD, shares, pure, or USD-per-shares. Example: `USD`. |
| `period` | string | yes | Frame period, such as CY2019, CY2019Q1, or CY2019Q1I. Example: `CY2024`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ccp": "string",
      "data": [
        {}
      ],
      "description": "string",
      "label": "string",
      "pts": 1,
      "tag": "string",
      "taxonomy": "string",
      "uom": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ccp` | string | Calendar period key. |
| `data` | array<object> | Frame data records. |
| `description` | string | Frame description. |
| `label` | string | Frame label. |
| `pts` | number | Number of data points. |
| `tag` | string | Taxonomy tag. |
| `taxonomy` | string | Taxonomy namespace. |
| `uom` | string | Unit of measure. |

## Native endpoint

Through the native United States Securities and Exchange Commission (SEC) EDGAR Database API, this operation is `GET https://data.sec.gov/api/xbrl/frames/[:taxonomy]/[:tag]/[:unit]/[:period].json` (base URL `https://www.sec.gov`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-xbrl-frame.md) for the provider-specific parameters and requirements.

