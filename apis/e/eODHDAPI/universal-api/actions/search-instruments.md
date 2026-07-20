# EODHD: Search Instruments

Finds instruments in EODHD API by keyword.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/search-instruments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/search-instruments?connectionId=$CONNECTION_ID&query=Apple" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "Apple"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/search-instruments?${params}`, {
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
| `query` | string | yes | Search query text for ticker, company, ETF, fund, or index lookup. Example: `Apple`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Code": "string",
      "Country": "string",
      "Currency": "string",
      "Exchange": "string",
      "ISIN": "string",
      "Name": "Ava Chen",
      "previousClose": 1,
      "previousCloseDate": "2026-05-07T12:00:00.000Z",
      "Type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | string | Instrument code. |
| `Country` | string | Country name. |
| `Currency` | string | Trading currency. |
| `Exchange` | string | Exchange code. |
| `ISIN` | string | ISIN when available. |
| `Name` | string | Instrument name. |
| `previousClose` | number | Previous close price when returned. |
| `previousCloseDate` | date | Previous close date when returned. |
| `Type` | string | Instrument type. |

## Native endpoint

Through the native EODHD API, this operation is `GET /search/{query}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-instruments.md) for the provider-specific parameters and requirements.

