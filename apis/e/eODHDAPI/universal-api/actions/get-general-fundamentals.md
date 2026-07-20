# EODHD: Get General Fundamentals

Retrieves general fundamentals for a symbol from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-general-fundamentals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-general-fundamentals?connectionId=$CONNECTION_ID&symbol=AAPL.US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "symbol": "AAPL.US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-general-fundamentals?${params}`, {
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
| `symbol` | string | yes | EODHD ticker in `{symbol}.{exchange}` format, such as `AAPL.US`. Example: `AAPL.US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Code": "string",
      "CountryISO": "string",
      "CountryName": "Ava Chen",
      "CurrencyCode": "string",
      "CurrencyName": "Ava Chen",
      "CurrencySymbol": "string",
      "Description": "string",
      "Exchange": "string",
      "FullTimeEmployees": 1,
      "Industry": "string",
      "ISIN": "string",
      "LogoURL": "https://example.com",
      "Name": "Ava Chen",
      "PrimaryTicker": "string",
      "Sector": "string",
      "Type": "string",
      "UpdatedAt": "2026-05-07T12:00:00.000Z",
      "WebURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | string | EODHD symbol code. |
| `CountryISO` | string | Country ISO code. |
| `CountryName` | string | Country name. |
| `CurrencyCode` | string | Currency code. |
| `CurrencyName` | string | Currency name. |
| `CurrencySymbol` | string | Currency symbol. |
| `Description` | string | Company description. |
| `Exchange` | string | Exchange code. |
| `FullTimeEmployees` | number | Full-time employee count. |
| `Industry` | string | Industry. |
| `ISIN` | string | ISIN. |
| `LogoURL` | string | Logo URL. |
| `Name` | string | Security or company name. |
| `PrimaryTicker` | string | Primary ticker. |
| `Sector` | string | Sector. |
| `Type` | string | Security type. |
| `UpdatedAt` | date | Last update date. |
| `WebURL` | string | Website URL. |

## Native endpoint

Through the native EODHD API, this operation is `GET /fundamentals/{symbol}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-general-fundamentals.md) for the provider-specific parameters and requirements.

