# Fatture in Cloud: Modify Supplier

Updates an existing supplier in Fatture in Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/modify-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fatture in Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/modify-supplier" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "supplierId": 1,
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/modify-supplier', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "supplierId": 1,
    "data": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | The ID of the company. |
| `supplierId` | number | yes | The ID of the supplier. |
| `data` | object | yes | The supplier payload inside the provider data envelope. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressCity": "string",
      "addressExtra": "string",
      "addressPostalCode": "string",
      "addressProvince": "string",
      "addressStreet": "string",
      "certifiedEmail": "ava@example.com",
      "code": "string",
      "contactPerson": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "fax": "string",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "taxCode": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vatNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressCity` | string |  |
| `addressExtra` | string |  |
| `addressPostalCode` | string |  |
| `addressProvince` | string |  |
| `addressStreet` | string |  |
| `certifiedEmail` | string |  |
| `code` | string |  |
| `contactPerson` | string |  |
| `country` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `fax` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `taxCode` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `vatNumber` | string |  |

## Native endpoint

Through the native Fatture in Cloud API, this operation is `PUT /c/:company_id/entities/suppliers/:supplier_id` (base URL `https://api-v2.fattureincloud.it`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-supplier.md) for the provider-specific parameters and requirements.

