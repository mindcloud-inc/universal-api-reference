# EODHD: Get Exchange Details

Retrieves trading hours and holidays for an exchange from EODHD API.

```
GET https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-exchange-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EODHD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-exchange-details?connectionId=$CONNECTION_ID&exchangeCode=US" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "exchangeCode": "US"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eODHDAPI/latest/actions/get-exchange-details?${params}`, {
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
| `exchangeCode` | string | yes | EODHD exchange code for exchange details. Example: `US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActiveTickers": 1,
      "Code": "string",
      "Country": "string",
      "Currency": "string",
      "Name": "Ava Chen",
      "OperatingMIC": "string",
      "PreviousDayUpdatedTickers": 1,
      "Timezone": "string",
      "UpdatedTickers": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActiveTickers` | number | Active ticker count. |
| `Code` | string | Exchange code. |
| `Country` | string | Country name. |
| `Currency` | string | Exchange currency. |
| `Name` | string | Exchange name. |
| `OperatingMIC` | string | Operating MIC. |
| `PreviousDayUpdatedTickers` | number | Previous-day updated ticker count. |
| `Timezone` | string | Exchange timezone. |
| `UpdatedTickers` | number | Updated ticker count. |

## Native endpoint

Through the native EODHD API, this operation is `GET /exchange-details/{exchangeCode}` (base URL `https://eodhd.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-exchange-details.md) for the provider-specific parameters and requirements.

