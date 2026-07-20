# Unleashed: Create Customer

Creates a new customer in Unleashed.

```
POST https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerCode": "string",
  "customerName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/create-customer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerCode": "string",
    "customerName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerCode` | string | yes | Unique code for the customer. |
| `customerName` | string | yes | Display name for the customer. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "contacts": [
        {}
      ],
      "creditLimit": 1,
      "currency": {},
      "customerCode": "string",
      "customerName": "Ava Chen",
      "customerType": "string",
      "defaultWarehouse": {},
      "discountRate": 1,
      "email": "ava@example.com",
      "guid": "string",
      "hasCreditLimit": true,
      "lastModifiedOn": "string",
      "notes": "string",
      "obsolete": true,
      "paymentTerm": "string",
      "phoneNumber": "string",
      "stopCredit": true,
      "taxable": true,
      "taxCode": "string",
      "taxRate": 1,
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `contacts` | array<object> |  |
| `creditLimit` | number |  |
| `currency` | object |  |
| `customerCode` | string |  |
| `customerName` | string |  |
| `customerType` | string |  |
| `defaultWarehouse` | object |  |
| `discountRate` | number |  |
| `email` | string |  |
| `guid` | string |  |
| `hasCreditLimit` | boolean |  |
| `lastModifiedOn` | string |  |
| `notes` | string |  |
| `obsolete` | boolean |  |
| `paymentTerm` | string |  |
| `phoneNumber` | string |  |
| `stopCredit` | boolean |  |
| `taxable` | boolean |  |
| `taxCode` | string |  |
| `taxRate` | number |  |
| `website` | string |  |

## Native endpoint

Through the native Unleashed API, this operation is `POST /Customers` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-customer.md) for the provider-specific parameters and requirements.

