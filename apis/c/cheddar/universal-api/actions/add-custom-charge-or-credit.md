# Cheddar: Add Custom Charge or Credit

Creates a custom charge or credit in Cheddar.

```
POST https://connect.mindcloud.co/v1/universal/cheddar/latest/actions/add-custom-charge-or-credit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cheddar `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerCode` | string | yes | Customer code from Cheddar. |
| `chargeCode` | string | yes | Code for the custom charge or credit. |
| `quantity` | number | yes | Positive integer quantity for the custom charge or credit. |
| `eachAmount` | number | yes | Positive or negative amount with two-digit decimal precision. |
| `description` | string | no | Description for the custom charge or credit. |
| `invoicePeriod` | string | no | Billing period: current (default) or outstanding. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `remoteAddress` | string | no | Client IPv4 address for fraud protection and rate limiting. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customers` | array<object> |  |
| `customers[].code` | string |  |
| `customers[].company` | string |  |
| `customers[].createdDatetime` | date |  |
| `customers[].email` | string |  |
| `customers[].firstName` | string |  |
| `customers[].gatewayToken` | string |  |
| `customers[].id` | string |  |
| `customers[].lastName` | string |  |
| `customers[].modifiedDatetime` | date |  |
| `customers[].notes` | string |  |
| `customers[].subscriptions` | array<object> |  |
| `customers[].subscriptions[].canceledDatetime` | date |  |
| `customers[].subscriptions[].ccExpirationDate` | date |  |
| `customers[].subscriptions[].ccFirstName` | string |  |
| `customers[].subscriptions[].ccLastFour` | string |  |
| `customers[].subscriptions[].ccLastName` | string |  |
| `customers[].subscriptions[].ccType` | string |  |
| `customers[].subscriptions[].createdDatetime` | date |  |
| `customers[].subscriptions[].gatewayToken` | string |  |
| `customers[].subscriptions[].id` | string |  |
| `customers[].subscriptions[].invoices` | array<object> |  |
| `customers[].subscriptions[].invoices[].billingDatetime` | date |  |
| `customers[].subscriptions[].invoices[].charges` | array<object> |  |
| `customers[].subscriptions[].invoices[].charges[].code` | string |  |
| `customers[].subscriptions[].invoices[].charges[].description` | string |  |
| `customers[].subscriptions[].invoices[].charges[].eachAmount` | number |  |
| `customers[].subscriptions[].invoices[].charges[].id` | string |  |
| `customers[].subscriptions[].invoices[].charges[].quantity` | number |  |
| `customers[].subscriptions[].invoices[].createdDatetime` | date |  |
| `customers[].subscriptions[].invoices[].id` | string |  |
| `customers[].subscriptions[].invoices[].number` | string |  |
| `customers[].subscriptions[].invoices[].transactions` | array<object> |  |
| `customers[].subscriptions[].invoices[].transactions[].amount` | number |  |
| `customers[].subscriptions[].invoices[].transactions[].id` | string |  |
| `customers[].subscriptions[].invoices[].transactions[].response` | string |  |
| `customers[].subscriptions[].invoices[].transactions[].transactedDatetime` | date |  |
| `customers[].subscriptions[].invoices[].type` | string |  |
| `customers[].subscriptions[].plans` | array<object> |  |
| `customers[].subscriptions[].plans[].code` | string |  |
| `customers[].subscriptions[].plans[].description` | string |  |
| `customers[].subscriptions[].plans[].id` | string |  |
| `customers[].subscriptions[].plans[].isActive` | boolean |  |
| `customers[].subscriptions[].plans[].isFree` | boolean |  |
| `customers[].subscriptions[].plans[].name` | string |  |
| `customers[].subscriptions[].plans[].trialDays` | number |  |

## Native endpoint

Through the native Cheddar API, this operation is `POST /customers/add-charge/productCode/{{credentials.productCode}}/code/:customerCode` (base URL `https://getcheddar.com/xml`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-custom-charge-or-credit.md) for the provider-specific parameters and requirements.

