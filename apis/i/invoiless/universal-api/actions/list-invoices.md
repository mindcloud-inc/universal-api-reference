# Invoiless: List Invoices

Retrieves invoices from Invoiless.

```
GET https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoiless `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/list-invoices?${params}`, {
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
| `search` | string | no | Search by invoice number, customer name, or tags. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__v": 1,
      "_id": "string",
      "acceptPayment": true,
      "attachments": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "customer": {
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
        "property": "string",
        "shipTo": {
          "company": "string",
          "email": "ava@example.com",
          "name": "Ava Chen",
          "shortName": "Ava Chen"
        }
      },
      "date": "2026-05-07T12:00:00.000Z",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isOverdue": true,
      "isRetainer": true,
      "items": [
        {
          "_id": "string",
          "id": "string",
          "name": "Ava Chen",
          "price": 1,
          "quantity": 1
        }
      ],
      "kind": "string",
      "lang": "string",
      "netTotal": 1,
      "notes": "string",
      "number": "string",
      "overdueAlertSent": true,
      "property": {
        "_id": "string",
        "id": "string"
      },
      "shipTo": true,
      "status": "string",
      "subTotal": 1,
      "tax": 1,
      "taxIncluded": true,
      "total": 1,
      "url": "https://example.com"
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
| `acceptPayment` | boolean |  |
| `attachments` | number |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `customer.__v` | number |  |
| `customer._id` | string |  |
| `customer.attachPdf` | boolean |  |
| `customer.billTo.company` | string |  |
| `customer.billTo.email` | string |  |
| `customer.billTo.name` | string |  |
| `customer.billTo.shortName` | string |  |
| `customer.createdAt` | date |  |
| `customer.email` | string |  |
| `customer.id` | string |  |
| `customer.property` | string |  |
| `customer.shipTo.company` | string |  |
| `customer.shipTo.email` | string |  |
| `customer.shipTo.name` | string |  |
| `customer.shipTo.shortName` | string |  |
| `date` | date |  |
| `dueDate` | date |  |
| `id` | string |  |
| `isOverdue` | boolean |  |
| `isRetainer` | boolean |  |
| `items[]._id` | string |  |
| `items[].id` | string |  |
| `items[].name` | string |  |
| `items[].price` | number |  |
| `items[].quantity` | number |  |
| `kind` | string |  |
| `lang` | string |  |
| `netTotal` | number |  |
| `notes` | string |  |
| `number` | string |  |
| `overdueAlertSent` | boolean |  |
| `property._id` | string |  |
| `property.id` | string |  |
| `shipTo` | boolean |  |
| `status` | string |  |
| `subTotal` | number |  |
| `tax` | number |  |
| `taxIncluded` | boolean |  |
| `total` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Invoiless API, this operation is `GET /invoices` (base URL `https://api.invoiless.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

