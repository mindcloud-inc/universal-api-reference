# Zoho Books: Get Bill



```
GET https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-bill
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Books `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-bill?connectionId=$CONNECTION_ID&bill_id=string&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bill_id": "string",
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBooks/latest/actions/get-bill?${params}`, {
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
| `bill_id` | string | yes | Unique identifier of the bill. |
| `organizationId` | string | yes | ID of the organization. |

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

Through the native Zoho Books API, this operation is `GET /bills/:bill_id` (base URL `https://www.zohoapis.com/books/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bill.md) for the provider-specific parameters and requirements.

