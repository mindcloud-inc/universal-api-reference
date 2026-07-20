# CDR Platform: Calculate CO2 Removal Price

Calculates CO2 removal pricing in CDR Platform.

```
GET https://connect.mindcloud.co/v1/universal/cDRPlatform/latest/actions/calculate-co2-removal-price
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CDR Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cDRPlatform/latest/actions/calculate-co2-removal-price?connectionId=$CONNECTION_ID&weightUnit=kg&currency=usd&items%5B%5D.methodType=forestation&items%5B%5D.cdrAmount=1000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "weightUnit": "kg",
  "currency": "usd",
  "items[].methodType": "forestation",
  "items[].cdrAmount": "1000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cDRPlatform/latest/actions/calculate-co2-removal-price?${params}`, {
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
| `weightUnit` | list<string> | yes | Unit for the CO2 removal amount. One of: `g`, `kg`, `t`. Example: `kg`. |
| `currency` | list<string> | yes | Currency for the price calculation. One of: `chf`, `eur`, `gbp`, `usd`. Example: `usd`. |
| `items[].methodType` | list<string> | yes | Carbon removal method type for an item. One of: `bio-oil`, `forestation`, `kelp-sinking`, `olivine`. Example: `forestation`. |
| `items[].cdrAmount` | number | yes | Amount of CO2 removal for an item, in the selected weight unit. Example: `1000`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cost": {
        "items": [
          {
            "cdr_amount": 1,
            "cost": 1,
            "method_type": "string"
          }
        ],
        "removal": 1,
        "total": 1,
        "variable_fees": 1
      },
      "currency": "string",
      "weight_unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cost` | object | Cost breakdown for the price calculation. |
| `cost.items` | array<object> | Per-removal-method price rows. |
| `cost.items[].cdr_amount` | number | Requested removal amount. |
| `cost.items[].cost` | number | Cost for this removal method item. |
| `cost.items[].method_type` | string | Removal method type. |
| `cost.removal` | number | Removal cost subtotal. |
| `cost.total` | number | Total calculated cost. |
| `cost.variable_fees` | number | Variable fees subtotal. |
| `currency` | string | Currency for the calculated cost. |
| `weight_unit` | string | Weight unit used in the calculation. |

## Native endpoint

Through the native CDR Platform API, this operation is `POST /v1/cdr/price/` (base URL `https://api.cdrplatform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-co2-removal-price.md) for the provider-specific parameters and requirements.

