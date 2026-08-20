# Centerpoint: Get Invoice



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-invoice?connectionId=$CONNECTION_ID&INVOICE_ID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "INVOICE_ID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-invoice?${params}`, {
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
| `INVOICE_ID` | string | yes |  |
| `include` | string | no |  |
| `fields[invoices]` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[transactions]` | string | no | Optional fields transactions query parameter. |
| `fields[productionDays]` | string | no | Optional fields production days query parameter. |
| `fields[products]` | string | no | Optional fields products query parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "amount": 1,
        "createdAt": "string",
        "deletedAt": {},
        "dueDate": {},
        "invoiceDate": "string",
        "isDraft": true,
        "isFinal": true,
        "jobHours": 1,
        "laborTravelCostTotal": 1,
        "laborTravelTotal": 1,
        "lastSentAt": {},
        "materialCostTotal": 1,
        "materialTotal": 1,
        "name": {},
        "options": {
          "billedAmount": 1,
          "billingAddress": "string",
          "checkoutName": "Ava Chen",
          "costSubtotal": 1,
          "costTotal": 1,
          "custom": [
            {}
          ],
          "descriptionFontSize": "string",
          "email": {
            "attachments": {
              "invoice": {},
              "otherFiles": [
                {}
              ],
              "siteBid": {}
            }
          },
          "isTaxExempt": true,
          "items": [
            {}
          ],
          "jobHours": 1,
          "laborTravelCostTotal": 1,
          "laborTravelTotal": 1,
          "margin": 1,
          "materialCostTotal": 1,
          "materialTotal": 1,
          "otherCostTotal": 1,
          "otherTotal": 1,
          "paymentTerms": "string",
          "profit": 1,
          "profitPerHour": 1,
          "propertyAddress": "string",
          "signature": "string",
          "subtotal": 1,
          "taxable": 1,
          "taxAmount": 1,
          "taxRate": 1,
          "total": 1,
          "view": "string"
        },
        "otherCostTotal": 1,
        "otherTotal": 1,
        "productionId": 1,
        "productionName": "Ava Chen",
        "profileId": 1,
        "profit": 1,
        "updatedAt": "string",
        "uuid": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.amount` | number |  |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.dueDate` | object |  |
| `attributes.invoiceDate` | string |  |
| `attributes.isDraft` | boolean |  |
| `attributes.isFinal` | boolean |  |
| `attributes.jobHours` | number |  |
| `attributes.laborTravelCostTotal` | number |  |
| `attributes.laborTravelTotal` | number |  |
| `attributes.lastSentAt` | object |  |
| `attributes.materialCostTotal` | number |  |
| `attributes.materialTotal` | number |  |
| `attributes.name` | object |  |
| `attributes.options.billedAmount` | number |  |
| `attributes.options.billingAddress` | string |  |
| `attributes.options.checkoutName` | string |  |
| `attributes.options.costSubtotal` | number |  |
| `attributes.options.costTotal` | number |  |
| `attributes.options.custom` | array<object> |  |
| `attributes.options.descriptionFontSize` | string |  |
| `attributes.options.email.attachments.invoice` | object |  |
| `attributes.options.email.attachments.otherFiles` | array<object> |  |
| `attributes.options.email.attachments.siteBid` | object |  |
| `attributes.options.isTaxExempt` | boolean |  |
| `attributes.options.items` | array<object> |  |
| `attributes.options.jobHours` | number |  |
| `attributes.options.laborTravelCostTotal` | number |  |
| `attributes.options.laborTravelTotal` | number |  |
| `attributes.options.margin` | number |  |
| `attributes.options.materialCostTotal` | number |  |
| `attributes.options.materialTotal` | number |  |
| `attributes.options.otherCostTotal` | number |  |
| `attributes.options.otherTotal` | number |  |
| `attributes.options.paymentTerms` | string |  |
| `attributes.options.profit` | number |  |
| `attributes.options.profitPerHour` | number |  |
| `attributes.options.propertyAddress` | string |  |
| `attributes.options.signature` | string |  |
| `attributes.options.subtotal` | number |  |
| `attributes.options.taxable` | number |  |
| `attributes.options.taxAmount` | number |  |
| `attributes.options.taxRate` | number |  |
| `attributes.options.total` | number |  |
| `attributes.options.view` | string |  |
| `attributes.otherCostTotal` | number |  |
| `attributes.otherTotal` | number |  |
| `attributes.productionId` | number |  |
| `attributes.productionName` | string |  |
| `attributes.profileId` | number |  |
| `attributes.profit` | number |  |
| `attributes.updatedAt` | string |  |
| `attributes.uuid` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET invoices/:INVOICE_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice.md) for the provider-specific parameters and requirements.

