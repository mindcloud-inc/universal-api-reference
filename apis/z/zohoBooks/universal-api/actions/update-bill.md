# Zoho Books: Update Bill



```
PUT https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-bill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-bill" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "bill_id": "string",
  "billNumber": "string",
  "organizationId": "string",
  "vendorId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/update-bill', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "bill_id": "string",
    "billNumber": "string",
    "organizationId": "string",
    "vendorId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bill_id` | string | yes | Unique identifier of the bill. |
| `billNumber` | string | yes | Bill number. |
| `lineItems[]` | array<object> | no | Line items of the bill. |
| `lineItems[].accountId` | string | no | Expense account for the bill line item. |
| `lineItems[].description` | string | no | Bill line item description. |
| `lineItems[].lineItemId` | string | no | Existing bill line item identifier. |
| `lineItems[].quantity` | number | no | Bill line item quantity. |
| `lineItems[].rate` | number | no | Bill line item rate. |
| `notes` | string | no | Notes for the bill. |
| `organizationId` | string | yes | ID of the organization. |
| `referenceNumber` | string | no | Reference number. |
| `vendorId` | string | yes | Vendor for the bill. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bill": {
        "accountId": "string",
        "accountName": "Ava Chen",
        "attachmentName": "Ava Chen",
        "balance": 1,
        "billId": "string",
        "billingAddress": {},
        "billNumber": "string",
        "createdTime": "2026-05-07T12:00:00.000Z",
        "currencyCode": "string",
        "currencyId": "string",
        "currencySymbol": "string",
        "currentSubStatus": "string",
        "date": "2026-05-07T12:00:00.000Z",
        "dueDate": "2026-05-07T12:00:00.000Z",
        "entityType": "string",
        "exchangeRate": 1,
        "lastModifiedTime": "2026-05-07T12:00:00.000Z",
        "lineItems": [
          {}
        ],
        "notes": "string",
        "paymentMade": 1,
        "pricePrecision": 1,
        "referenceNumber": "string",
        "status": "string",
        "subTotal": 1,
        "taxTotal": 1,
        "templateId": "string",
        "templateName": "Ava Chen",
        "total": 1,
        "vendorCreditsApplied": 1,
        "vendorId": "string",
        "vendorName": "Ava Chen"
      },
      "code": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bill.accountId` | string |  |
| `bill.accountName` | string |  |
| `bill.attachmentName` | string |  |
| `bill.balance` | number |  |
| `bill.billId` | string |  |
| `bill.billingAddress` | object |  |
| `bill.billNumber` | string |  |
| `bill.createdTime` | date |  |
| `bill.currencyCode` | string |  |
| `bill.currencyId` | string |  |
| `bill.currencySymbol` | string |  |
| `bill.currentSubStatus` | string |  |
| `bill.date` | date |  |
| `bill.dueDate` | date |  |
| `bill.entityType` | string |  |
| `bill.exchangeRate` | number |  |
| `bill.lastModifiedTime` | date |  |
| `bill.lineItems` | array<object> |  |
| `bill.notes` | string |  |
| `bill.paymentMade` | number |  |
| `bill.pricePrecision` | number |  |
| `bill.referenceNumber` | string |  |
| `bill.status` | string |  |
| `bill.subTotal` | number |  |
| `bill.taxTotal` | number |  |
| `bill.templateId` | string |  |
| `bill.templateName` | string |  |
| `bill.total` | number |  |
| `bill.vendorCreditsApplied` | number |  |
| `bill.vendorId` | string |  |
| `bill.vendorName` | string |  |
| `code` | number |  |
| `message` | string |  |

## Native endpoint

Through the native Zoho Books API, this operation is `PUT /bills/:bill_id` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-bill.md) for the provider-specific parameters and requirements.

