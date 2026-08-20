# Centerpoint: List Invoices



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-invoices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-invoices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-invoices?${params}`, {
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
| `filter[lastSentAt]` | string | no | Start of the “Last Sent At” date range (inclusive). Example: `YYYY-MM-DD HH:MM:SS`. |
| `filter[lastSentAt][lt]` | string | no | End of the “Last Sent At” date range (exclusive / less-than). Example: `YYYY-MM-DD HH:MM:SS`. |
| `filter[lastSentAt][timezone]` | string | no | Default: `America/Chicago`. |
| `include` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[productions]` | string | no | Optional fields productions query parameter. |
| `fields[properties]` | string | no | Optional fields properties query parameter. |
| `fields[companies]` | string | no | Optional fields companies query parameter. |
| `fields[employees]` | string | no | Optional fields employees query parameter. |
| `fields[profiles]` | string | no | Optional fields profiles query parameter. |
| `aggregates[subtotal][0]` | string | no | Optional aggregates subtotal 0 query parameter. |
| `aggregates[amount][0]` | string | no | Optional aggregates amount 0 query parameter. |
| `aggregates[margin][0]` | string | no | Optional aggregates margin 0 query parameter. |
| `aggregates[cost][0]` | string | no | Optional aggregates cost 0 query parameter. |

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

Through the native Centerpoint API, this operation is `GET invoices` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-invoices.md) for the provider-specific parameters and requirements.

