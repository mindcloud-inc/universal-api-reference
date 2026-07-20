# EODHD: List Exchange Symbols

Retrieves symbols for an exchange from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-exchange-symbols
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-exchange-symbols?connectionId=$CONNECTION_ID&exchangeCode=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exchangeCode": "US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-exchange-symbols?${params}`, {
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
| `exchangeCode` | string | yes | EODHD exchange code, such as `US`, `LSE`, `CC`, or `FOREX`. Example: `US`. |

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
      "Isin": "string",
      "Name": "Ava Chen",
      "Type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | string | Ticker or instrument code. |
| `Country` | string | Country name. |
| `Currency` | string | Trading currency. |
| `Exchange` | string | Exchange code. |
| `Isin` | string | ISIN when available. |
| `Name` | string | Instrument display name. |
| `Type` | string | Instrument type. |

## Native endpoint

Through the native EODHD API, this operation is `GET /exchange-symbol-list/{exchangeCode}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-exchange-symbols.md) for the provider-specific parameters and requirements.

