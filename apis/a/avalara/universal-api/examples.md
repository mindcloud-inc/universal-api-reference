# Avalara AvaTax Universal API Examples

These examples use the MindCloud API key and Avalara AvaTax connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Test Connection



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/test-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/avalara/latest/actions/test-connection?${params}`, {
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
      "authenticated": true,
      "authenticatedAccountId": 1,
      "authenticatedUserId": 1,
      "authenticatedUserName": "Ava Chen",
      "authenticationType": "string",
      "crmid": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Test Connection action reference](actions/test-connection.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/avalara/latest/actions/test-connection).

## Create Transaction



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/avalara/latest/actions/create-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lines[]": [
    "string"
  ],
  "lines[].amount": 1,
  "customerCode": "string",
  "date": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/avalara/latest/actions/create-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lines[]": ["string"],
    "lines[].amount": 1,
    "customerCode": "string",
    "date": "2026-05-07T12:00:00.000Z"
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
      "addresses": [
        {}
      ],
      "adjustmentDescription": "string",
      "adjustmentReason": "string",
      "batchCode": "string",
      "businessIdentificationNo": "string",
      "code": "string",
      "companyId": 1,
      "country": "string",
      "currencyCode": "string",
      "customerCode": "string",
      "customerUsageType": "string",
      "customerVendorCode": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "destinationAddressId": 1,
      "email": "ava@example.com",
      "entityUseCode": "string",
      "exchangeRate": 1,
      "exchangeRateCurrencyCode": "string",
      "exchangeRateEffectiveDate": "2026-05-07T12:00:00.000Z",
      "exemptNo": "string",
      "id": 1,
      "isSellerImporterOfRecord": true,
      "lines": [
        {}
      ],
      "locationCode": "string",
      "locationTypes": [
        {}
      ],
      "locked": true,
      "messages": [
        {}
      ],
      "modifiedDate": "2026-05-07T12:00:00.000Z",
      "modifiedUserId": 1,
      "originAddressId": 1,
      "paymentDate": "2026-05-07T12:00:00.000Z",
      "purchaseOrderNo": "string",
      "reconciled": true,
      "referenceCode": "string",
      "region": "string",
      "reportingLocationCode": "string",
      "salespersonCode": "string",
      "shippingTaxes": [
        {}
      ],
      "softwareVersion": "string",
      "status": "string",
      "summary": [
        {}
      ],
      "taxDate": "2026-05-07T12:00:00.000Z",
      "taxOverrideAmount": 1,
      "taxOverrideReason": "string",
      "taxOverrideType": "string",
      "totalAmount": 1,
      "totalDiscount": 1,
      "totalExempt": 1,
      "totalTax": 1,
      "totalTaxable": 1,
      "totalTaxCalculated": 1,
      "type": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Transaction action reference](actions/create-transaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/avalara/latest/actions/create-transaction).
