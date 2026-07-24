# Rillion Prime Pay: List Payment Suppliers



```
GET https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-suppliers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/list-payment-suppliers?${params}`, {
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
| `searchTerm` | string | no | Filter suppliers by search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "internationalDetails": {},
      "paymentMethod": "string",
      "statusLastChanged": "string",
      "supplier": "string",
      "supplierAddress": {
        "address1": "string",
        "address2": {},
        "address3": {},
        "address4": {},
        "address5": "string",
        "address6": {},
        "country": {}
      },
      "supplierId": 1,
      "supplierName": "Ava Chen",
      "supplierPaymentGrouping": "string",
      "supplierRemitAddress": {
        "careOf": {},
        "city": "string",
        "country": "string",
        "postalCode": {},
        "state": "string",
        "street1": "string",
        "street2": "string",
        "zipCode": "string"
      },
      "supplierStatus": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `internationalDetails` | object |  |
| `paymentMethod` | string |  |
| `statusLastChanged` | string |  |
| `supplier` | string |  |
| `supplierAddress.address1` | string |  |
| `supplierAddress.address2` | object |  |
| `supplierAddress.address3` | object |  |
| `supplierAddress.address4` | object |  |
| `supplierAddress.address5` | string |  |
| `supplierAddress.address6` | object |  |
| `supplierAddress.country` | object |  |
| `supplierId` | number |  |
| `supplierName` | string |  |
| `supplierPaymentGrouping` | string |  |
| `supplierRemitAddress.careOf` | object |  |
| `supplierRemitAddress.city` | string |  |
| `supplierRemitAddress.country` | string |  |
| `supplierRemitAddress.postalCode` | object |  |
| `supplierRemitAddress.state` | string |  |
| `supplierRemitAddress.street1` | string |  |
| `supplierRemitAddress.street2` | string |  |
| `supplierRemitAddress.zipCode` | string |  |
| `supplierStatus` | string |  |

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `GET /payment/supplier` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-payment-suppliers.md) for the provider-specific parameters and requirements.

