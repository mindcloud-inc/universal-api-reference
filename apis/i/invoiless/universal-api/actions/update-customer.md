# Invoiless: Update Customer

Updates an existing customer in Invoiless.

```
PUT https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/update-customer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoiless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/update-customer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "billTo": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/update-customer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "billTo": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Customer id. |
| `billTo` | object | yes | Billing address object. Either firstName and lastName, or company, is required inside this object. |
| `shipTo` | object | no | Shipping address object. |
| `cc[]` | array<string> | no | Cc recipients. |
| `bcc[]` | array<string> | no | Bcc recipients. |
| `currency` | string | no | ISO 4217 currency code. |
| `lang` | string | no | Customer language code. |
| `dateFormat` | string | no | Preferred date format. |
| `attachPdf` | boolean | no | Attach a PDF copy to emails. |
| `notes` | string | no | Private notes. |
| `tags[]` | array<string> | no | Tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__v": 1,
      "_id": "string",
      "attachPdf": true,
      "billTo": {
        "company": "string",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "shortName": "Ava Chen"
      },
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "notes": "string",
      "property": "string",
      "shipTo": {
        "company": "string",
        "email": "ava@example.com",
        "name": "Ava Chen",
        "shortName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__v` | number |  |
| `_id` | string |  |
| `attachPdf` | boolean |  |
| `billTo.company` | string |  |
| `billTo.email` | string |  |
| `billTo.name` | string |  |
| `billTo.shortName` | string |  |
| `createdAt` | date |  |
| `email` | string |  |
| `id` | string |  |
| `notes` | string |  |
| `property` | string |  |
| `shipTo.company` | string |  |
| `shipTo.email` | string |  |
| `shipTo.name` | string |  |
| `shipTo.shortName` | string |  |

## Native endpoint

Through the native Invoiless API, this operation is `PUT /customers/:id` (base URL `https://api.invoiless.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-customer.md) for the provider-specific parameters and requirements.

