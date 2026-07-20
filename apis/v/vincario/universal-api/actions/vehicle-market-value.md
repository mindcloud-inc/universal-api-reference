# Vincario: Vehicle Market Value



```
GET https://connect.mindcloud.co/v1/universal/vincario/latest/actions/vehicle-market-value
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vincario `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vincario/latest/actions/vehicle-market-value?connectionId=$CONNECTION_ID&vin=1HGCM82633A004352" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "vin": "1HGCM82633A004352"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vincario/latest/actions/vehicle-market-value?${params}`, {
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
| `vin` | string | yes | Vehicle Identification Number. Example: `1HGCM82633A004352`. |
| `odometer` | number | no | Optional odometer reading used for price-adjusted calculations. Example: `120000`. |
| `odometerUnit` | string | no | Optional odometer unit. Supported values are km or mi. Example: `km`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "balance": {},
      "marketOdometer": {},
      "marketPrice": {},
      "period": {},
      "price": 1,
      "priceCurrency": "string",
      "records": [
        {}
      ],
      "vehicle": {},
      "vin": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | object |  |
| `marketOdometer` | object |  |
| `marketPrice` | object |  |
| `period` | object |  |
| `price` | number |  |
| `priceCurrency` | string |  |
| `records` | array<object> |  |
| `vehicle` | object |  |
| `vin` | string |  |

## Native endpoint

Through the native Vincario API, this operation is `GET /:apiKey/:controlSum/vehicle-market-value/:vin.:format` (base URL `https://api.vincario.com/3.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/vehicle-market-value.md) for the provider-specific parameters and requirements.

