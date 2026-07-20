# Unleashed: Get Customer

Retrieves a customer from your Unleashed customer directory.

```
GET https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/get-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/get-customer?connectionId=$CONNECTION_ID&customerGuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerGuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/get-customer?${params}`, {
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
| `customerGuid` | string | yes | The Unleashed customer GUID. |

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

Through the native Unleashed API, this operation is `GET /Customers/:customerGuid` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer.md) for the provider-specific parameters and requirements.

