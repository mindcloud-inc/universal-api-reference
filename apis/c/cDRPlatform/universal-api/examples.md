# CDR Platform Universal API Examples

These examples use the MindCloud API key and CDR Platform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Calculate CO2 Removal Price

Calculates CO2 removal pricing in CDR Platform.

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

Example response:

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

See the full [Calculate CO2 Removal Price action reference](actions/calculate-co2-removal-price.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cDRPlatform/latest/actions/calculate-co2-removal-price).

## Purchase CO2 Removal

Creates a CO2 removal purchase in CDR Platform.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cDRPlatform/latest/actions/purchase-co2-removal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "weightUnit": "kg",
  "currency": "usd",
  "items[].methodType": "forestation",
  "items[].cdrAmount": "1000"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cDRPlatform/latest/actions/purchase-co2-removal', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "weightUnit": "kg",
    "currency": "usd",
    "items[].methodType": "forestation",
    "items[].cdrAmount": "1000"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "transaction_uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Purchase CO2 Removal action reference](actions/purchase-co2-removal.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cDRPlatform/latest/actions/purchase-co2-removal).
