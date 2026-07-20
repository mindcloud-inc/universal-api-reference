# Cheddar Universal API Examples

These examples use the MindCloud API key and Cheddar connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Pricing Plans

Retrieves pricing plan records from Cheddar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/list-pricing-plans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/list-pricing-plans?${params}`, {
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
      "plans": [
        {
          "billingFrequency": "string",
          "billingFrequencyQuantity": 1,
          "code": "string",
          "createdDatetime": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": "string",
          "isActive": true,
          "isFree": true,
          "items": [
            {
              "code": "string",
              "createdDatetime": "2026-05-07T12:00:00.000Z",
              "id": "string",
              "isPeriodic": true,
              "name": "Ava Chen",
              "overageAmount": 1,
              "quantityIncluded": 1
            }
          ],
          "name": "Ava Chen",
          "recurringChargeAmount": 1,
          "recurringChargeCode": "string",
          "setupChargeAmount": 1,
          "setupChargeCode": "string",
          "trialDays": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Pricing Plans action reference](actions/list-pricing-plans.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cheddar/latest/actions/list-pricing-plans).

## Add Custom Charge or Credit

Creates a custom charge or credit in Cheddar.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/add-custom-charge-or-credit" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerCode": "string",
  "chargeCode": "string",
  "quantity": 1,
  "eachAmount": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/add-custom-charge-or-credit', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerCode": "string",
    "chargeCode": "string",
    "quantity": 1,
    "eachAmount": 1
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
      "customers": [
        {
          "code": "string",
          "company": "string",
          "createdDatetime": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "firstName": "Ava",
          "gatewayToken": "string",
          "id": "string",
          "lastName": "Chen",
          "modifiedDatetime": "2026-05-07T12:00:00.000Z",
          "notes": "string",
          "subscriptions": [
            {
              "canceledDatetime": "2026-05-07T12:00:00.000Z",
              "ccExpirationDate": "2026-05-07T12:00:00.000Z",
              "ccFirstName": "Ava",
              "ccLastFour": "string",
              "ccLastName": "Chen",
              "ccType": "string",
              "createdDatetime": "2026-05-07T12:00:00.000Z",
              "gatewayToken": "string",
              "id": "string",
              "invoices": [
                {
                  "billingDatetime": "2026-05-07T12:00:00.000Z",
                  "charges": [
                    {
                      "code": "string",
                      "description": "string",
                      "eachAmount": 1,
                      "id": "string",
                      "quantity": 1
                    }
                  ],
                  "createdDatetime": "2026-05-07T12:00:00.000Z",
                  "id": "string",
                  "number": "string",
                  "transactions": [
                    {
                      "amount": 1,
                      "id": "string",
                      "response": "string",
                      "transactedDatetime": "2026-05-07T12:00:00.000Z"
                    }
                  ],
                  "type": "string"
                }
              ],
              "plans": [
                {
                  "code": "string",
                  "description": "string",
                  "id": "string",
                  "isActive": true,
                  "isFree": true,
                  "name": "Ava Chen",
                  "trialDays": 1
                }
              ]
            }
          ]
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Custom Charge or Credit action reference](actions/add-custom-charge-or-credit.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cheddar/latest/actions/add-custom-charge-or-credit).
