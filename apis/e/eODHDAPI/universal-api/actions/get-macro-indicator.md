# EODHD: Get Macro Indicator

Retrieves a macroeconomic indicator by country from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-macro-indicator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-macro-indicator?connectionId=$CONNECTION_ID&country=USA&indicator=gdp_current_usd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country": "USA",
  "indicator": "gdp_current_usd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-macro-indicator?${params}`, {
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
| `country` | string | yes | Country code accepted by EODHD macro indicators, such as `USA`. Example: `USA`. |
| `indicator` | string | yes | Macro indicator code, for example gdp_current_usd. Example: `gdp_current_usd`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Indicator date. |
| `value` | number | Macro indicator value. |

## Native endpoint

Through the native EODHD API, this operation is `GET /macro-indicator/{country}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-macro-indicator.md) for the provider-specific parameters and requirements.

