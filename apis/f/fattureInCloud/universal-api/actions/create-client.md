# Fatture in Cloud: Create Client

Creates a new client in Fatture in Cloud.

```
POST https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/create-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fatture in Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "data": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fattureInCloud/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
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
| `data` | object | yes | The client payload inside the provider data envelope. |

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
      "bankIban": "string",
      "bankName": "Ava Chen",
      "bankSwiftCode": "string",
      "certifiedEmail": "ava@example.com",
      "code": "string",
      "contactPerson": "string",
      "country": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultPaymentMethod": {
        "id": 1,
        "name": "Ava Chen"
      },
      "defaultPaymentTerms": 1,
      "defaultPaymentTermsType": "string",
      "defaultVat": {
        "description": "string",
        "id": 1,
        "isDisabled": true,
        "value": 1
      },
      "eiCode": "string",
      "eInvoice": true,
      "email": "ava@example.com",
      "fax": "string",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "name": "Ava Chen",
      "notes": "string",
      "phone": "string",
      "shippingAddress": "string",
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
| `bankIban` | string |  |
| `bankName` | string |  |
| `bankSwiftCode` | string |  |
| `certifiedEmail` | string |  |
| `code` | string |  |
| `contactPerson` | string |  |
| `country` | string |  |
| `createdAt` | date |  |
| `defaultPaymentMethod.id` | number |  |
| `defaultPaymentMethod.name` | string |  |
| `defaultPaymentTerms` | number |  |
| `defaultPaymentTermsType` | string |  |
| `defaultVat.description` | string |  |
| `defaultVat.id` | number |  |
| `defaultVat.isDisabled` | boolean |  |
| `defaultVat.value` | number |  |
| `eiCode` | string |  |
| `eInvoice` | boolean |  |
| `email` | string |  |
| `fax` | string |  |
| `firstName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `name` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `shippingAddress` | string |  |
| `taxCode` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `vatNumber` | string |  |

## Native endpoint

Through the native Fatture in Cloud API, this operation is `POST /c/:company_id/entities/clients` (base URL `https://api-v2.fattureincloud.it`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client.md) for the provider-specific parameters and requirements.

