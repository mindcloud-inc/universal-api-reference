# Finnhub: Get Company Profile

Retrieves a company profile from Finnhub.

```
GET https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-company-profile
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Finnhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-company-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/finnhub/latest/actions/get-company-profile?${params}`, {
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
| `symbol` | string | no | Company symbol, such as AAPL. Example: `e.g. AAPL`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isin` | string | no | Optional ISIN identifier for the company. Example: `e.g. US0378331005`. |
| `cusip` | string | no | Optional CUSIP identifier for the company. Example: `e.g. 037833100`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "currency": "string",
      "estimateCurrency": "string",
      "exchange": "string",
      "finnhubIndustry": "string",
      "ipo": "2026-05-07T12:00:00.000Z",
      "logo": "string",
      "marketCapitalization": 1,
      "name": "Ava Chen",
      "phone": "string",
      "shareOutstanding": 1,
      "ticker": "string",
      "weburl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `currency` | string |  |
| `estimateCurrency` | string |  |
| `exchange` | string |  |
| `finnhubIndustry` | string |  |
| `ipo` | date |  |
| `logo` | string |  |
| `marketCapitalization` | number |  |
| `name` | string |  |
| `phone` | string |  |
| `shareOutstanding` | number |  |
| `ticker` | string |  |
| `weburl` | string |  |

## Native endpoint

Through the native Finnhub API, this operation is `GET /stock/profile2` (base URL `https://finnhub.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-profile.md) for the provider-specific parameters and requirements.

