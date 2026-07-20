# Invoiless: Get Invoice

Retrieves an invoice from Invoiless.

```
GET https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoiless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/get-invoice?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiless/latest/actions/get-invoice?${params}`, {
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
| `id` | string | yes | Invoice id. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__v": 1,
      "_id": "string",
      "acceptPayment": true,
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
      "formattedNotes": "string",
      "id": "string",
      "isOverdue": true,
      "isRetainer": true,
      "items": [
        {
          "_id": "string",
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
        "__v": 1,
        "_id": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "currencies": [
          "string"
        ],
        "currency": "string",
        "currencyDisplay": "string",
        "dateFormat": "string",
        "id": "string",
        "invoice": {
          "acceptPayment": true,
          "dueAfter": 1,
          "estimate": {
            "dueAfter": 1
          },
          "fractionDigits": true,
          "lang": "string",
          "qrCode": true,
          "recurring": {
            "acceptPayments": true,
            "automaticPayments": true,
            "dueAfter": 1,
            "globalLateFee": true,
            "globalReminders": true,
            "sendEmail": true
          },
          "retainer": {
            "dueAfter": 1
          },
          "showStatus": true,
          "taxIncluded": true,
          "taxPercentage": true,
          "theme": {
            "applyToDashboard": true,
            "color": {
              "type": "string",
              "value": "string"
            },
            "fixedFooter": true,
            "logo": true,
            "logoSize": "string",
            "padding": "string",
            "payButton": {
              "color": {
                "type": "string",
                "value": "string"
              },
              "position": "string"
            },
            "scale": 1,
            "shareButton": true
          }
        },
        "name": "Ava Chen",
        "onboarding": true,
        "swissQrBill": {
          "enabled": true
        },
        "xrechnung": {
          "enabled": true
        }
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
| `formattedNotes` | string |  |
| `id` | string |  |
| `isOverdue` | boolean |  |
| `isRetainer` | boolean |  |
| `items[]._id` | string |  |
| `items[].name` | string |  |
| `items[].price` | number |  |
| `items[].quantity` | number |  |
| `kind` | string |  |
| `lang` | string |  |
| `netTotal` | number |  |
| `notes` | string |  |
| `number` | string |  |
| `overdueAlertSent` | boolean |  |
| `property.__v` | number |  |
| `property._id` | string |  |
| `property.createdAt` | date |  |
| `property.currencies[]` | string |  |
| `property.currency` | string |  |
| `property.currencyDisplay` | string |  |
| `property.dateFormat` | string |  |
| `property.id` | string |  |
| `property.invoice.acceptPayment` | boolean |  |
| `property.invoice.dueAfter` | number |  |
| `property.invoice.estimate.dueAfter` | number |  |
| `property.invoice.fractionDigits` | boolean |  |
| `property.invoice.lang` | string |  |
| `property.invoice.qrCode` | boolean |  |
| `property.invoice.recurring.acceptPayments` | boolean |  |
| `property.invoice.recurring.automaticPayments` | boolean |  |
| `property.invoice.recurring.dueAfter` | number |  |
| `property.invoice.recurring.globalLateFee` | boolean |  |
| `property.invoice.recurring.globalReminders` | boolean |  |
| `property.invoice.recurring.sendEmail` | boolean |  |
| `property.invoice.retainer.dueAfter` | number |  |
| `property.invoice.showStatus` | boolean |  |
| `property.invoice.taxIncluded` | boolean |  |
| `property.invoice.taxPercentage` | boolean |  |
| `property.invoice.theme.applyToDashboard` | boolean |  |
| `property.invoice.theme.color.type` | string |  |
| `property.invoice.theme.color.value` | string |  |
| `property.invoice.theme.fixedFooter` | boolean |  |
| `property.invoice.theme.logo` | boolean |  |
| `property.invoice.theme.logoSize` | string |  |
| `property.invoice.theme.padding` | string |  |
| `property.invoice.theme.payButton.color.type` | string |  |
| `property.invoice.theme.payButton.color.value` | string |  |
| `property.invoice.theme.payButton.position` | string |  |
| `property.invoice.theme.scale` | number |  |
| `property.invoice.theme.shareButton` | boolean |  |
| `property.name` | string |  |
| `property.onboarding` | boolean |  |
| `property.swissQrBill.enabled` | boolean |  |
| `property.xrechnung.enabled` | boolean |  |
| `shipTo` | boolean |  |
| `status` | string |  |
| `subTotal` | number |  |
| `tax` | number |  |
| `taxIncluded` | boolean |  |
| `total` | number |  |
| `url` | string |  |

## Native endpoint

Through the native Invoiless API, this operation is `GET /invoices/:id` (base URL `https://api.invoiless.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

