# EODHD: List Supported Exchanges

Retrieves supported exchanges from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-supported-exchanges
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-supported-exchanges?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/list-supported-exchanges?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "Code": "string",
      "Country": "string",
      "CountryISO2": "string",
      "CountryISO3": "string",
      "Currency": "string",
      "Name": "Ava Chen",
      "OperatingMIC": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | string | EODHD exchange code. |
| `Country` | string | Country name. |
| `CountryISO2` | string | ISO alpha-2 country code. |
| `CountryISO3` | string | ISO alpha-3 country code. |
| `Currency` | string | Exchange currency code. |
| `Name` | string | Exchange display name. |
| `OperatingMIC` | string | Operating MIC code or comma-separated MIC list. |

## Native endpoint

Through the native EODHD API, this operation is `GET /exchanges-list/` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-supported-exchanges.md) for the provider-specific parameters and requirements.

