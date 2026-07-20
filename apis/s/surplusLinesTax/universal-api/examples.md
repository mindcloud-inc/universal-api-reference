# Surplus Lines Tax Universal API Examples

These examples use the MindCloud API key and Surplus Lines Tax connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Retrieve Historical Surplus Lines Tax Rates



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surplusLinesTax/latest/actions/retrieve-historical-surplus-lines-tax-rates?connectionId=$CONNECTION_ID&state=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "state": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surplusLinesTax/latest/actions/retrieve-historical-surplus-lines-tax-rates?${params}`, {
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
      "account": {
        "balance": "string",
        "freeQueriesRemaining": 1,
        "wasFreeQuery": true
      },
      "queryDate": "2026-05-07T12:00:00.000Z",
      "rate": {
        "confidence": "string",
        "dataSource": "string",
        "effectiveFrom": "2026-05-07T12:00:00.000Z",
        "fieldSources": {
          "filingFee": "string",
          "fireMarshalTax": "string",
          "flatFee": "string",
          "regulatoryFee": "string",
          "roundingRule": "string",
          "serviceFee": "string",
          "slasClearinghouseFee": "string",
          "specialNotes": "string",
          "stampingFee": "string",
          "surcharge": "string",
          "taxRate": "string"
        },
        "filingFee": "string",
        "fireMarshalTax": "string",
        "flatFee": "string",
        "legislativeSource": "string",
        "regulatoryFee": "string",
        "roundingRule": "string",
        "serviceFee": "string",
        "slasClearinghouseFee": "string",
        "stampingFee": "string",
        "surcharge": "string",
        "taxRate": "string"
      },
      "ratesFrom": "string",
      "state": "string",
      "stateCode": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Retrieve Historical Surplus Lines Tax Rates action reference](actions/retrieve-historical-surplus-lines-tax-rates.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/surplusLinesTax/latest/actions/retrieve-historical-surplus-lines-tax-rates).

## Calculate Surplus Lines Taxes



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/surplusLinesTax/latest/actions/calculate-surplus-lines-taxes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "state": "string",
  "premium": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/surplusLinesTax/latest/actions/calculate-surplus-lines-taxes', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "state": "string",
    "premium": 1
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
      "account": {
        "balance": "string",
        "freeQueriesRemaining": 1,
        "wasFreeQuery": true
      },
      "breakdown": {
        "baseTax": {
          "amount": 1,
          "rate": "string"
        },
        "fireMarshalTax": {
          "amount": 1,
          "rate": "string"
        },
        "flatFee": {
          "amount": 1,
          "rate": "string"
        },
        "stampingFee": {
          "amount": 1,
          "rate": "string"
        }
      },
      "legislativeSource": "string",
      "notes": [
        "string"
      ],
      "premium": 1,
      "ratesFrom": "string",
      "state": "string",
      "stateCode": "string",
      "success": true,
      "totalDue": 1,
      "totalTax": 1
    }
  ],
  "meta": {}
}
```

See the full [Calculate Surplus Lines Taxes action reference](actions/calculate-surplus-lines-taxes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/surplusLinesTax/latest/actions/calculate-surplus-lines-taxes).
