# Clockify: Update Invoice Settings

Updates workspace invoice settings in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-invoice-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-invoice-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "labels": {},
  "defaults.notes": "string",
  "defaults.subject": "string",
  "labels.amount": "string",
  "labels.billFrom": "string",
  "labels.billTo": "string",
  "labels.description": "string",
  "labels.discount": "string",
  "labels.dueDate": "string",
  "labels.issueDate": "string",
  "labels.itemType": "string",
  "labels.notes": "string",
  "labels.paid": "string",
  "labels.quantity": "string",
  "labels.subtotal": "string",
  "labels.tax": "string",
  "labels.tax2": "string",
  "labels.total": "string",
  "labels.totalAmountDue": "string",
  "labels.unitPrice": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/update-invoice-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "labels": {},
    "defaults.notes": "string",
    "defaults.subject": "string",
    "labels.amount": "string",
    "labels.billFrom": "string",
    "labels.billTo": "string",
    "labels.description": "string",
    "labels.discount": "string",
    "labels.dueDate": "string",
    "labels.issueDate": "string",
    "labels.itemType": "string",
    "labels.notes": "string",
    "labels.paid": "string",
    "labels.quantity": "string",
    "labels.subtotal": "string",
    "labels.tax": "string",
    "labels.tax2": "string",
    "labels.total": "string",
    "labels.totalAmountDue": "string",
    "labels.unitPrice": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | list<string> | yes |  |
| `labels` | object | yes |  |
| `defaults` | object | no |  |
| `exportFields` | object | no |  |
| `defaults.companyId` | string | no |  |
| `defaults.dueDays` | number | no |  |
| `defaults.itemTypeId` | string | no |  |
| `defaults.notes` | string | yes |  |
| `defaults.subject` | string | yes |  |
| `defaults.tax2Percent` | number | no |  |
| `defaults.taxPercent` | number | no |  |
| `defaults.taxType` | string | no |  |
| `exportFields.itemType` | boolean | no |  |
| `exportFields.quantity` | boolean | no |  |
| `exportFields.rtl` | boolean | no |  |
| `exportFields.tax` | boolean | no |  |
| `exportFields.tax2` | boolean | no |  |
| `exportFields.unitPrice` | boolean | no |  |
| `labels.amount` | string | yes |  |
| `labels.billFrom` | string | yes |  |
| `labels.billTo` | string | yes |  |
| `labels.description` | string | yes |  |
| `labels.discount` | string | yes |  |
| `labels.dueDate` | string | yes |  |
| `labels.issueDate` | string | yes |  |
| `labels.itemType` | string | yes |  |
| `labels.notes` | string | yes |  |
| `labels.paid` | string | yes |  |
| `labels.quantity` | string | yes |  |
| `labels.subtotal` | string | yes |  |
| `labels.tax` | string | yes |  |
| `labels.tax2` | string | yes |  |
| `labels.total` | string | yes |  |
| `labels.totalAmountDue` | string | yes |  |
| `labels.unitPrice` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaults": {
        "companyId": "string",
        "defaultImportExpenseItemTypeId": "string",
        "defaultImportTimeItemTypeId": "string",
        "dueDays": 1,
        "itemType": "string",
        "itemTypeId": "string",
        "notes": "string",
        "subject": "string",
        "tax": 1,
        "tax2": 1,
        "tax2Percent": 1,
        "taxPercent": 1,
        "taxType": "string"
      },
      "exportFields": {
        "itemType": true,
        "quantity": true,
        "rtl": true,
        "tax": true,
        "tax2": true,
        "unitPrice": true
      },
      "labels": {
        "amount": "string",
        "billFrom": "string",
        "billTo": "string",
        "description": "string",
        "discount": "string",
        "dueDate": "string",
        "issueDate": "string",
        "itemType": "string",
        "notes": "string",
        "paid": "string",
        "quantity": "string",
        "subtotal": "string",
        "tax": "string",
        "tax2": "string",
        "total": "string",
        "totalAmount": "string",
        "unitPrice": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaults` | object |  |
| `defaults.companyId` | string |  |
| `defaults.defaultImportExpenseItemTypeId` | string |  |
| `defaults.defaultImportTimeItemTypeId` | string |  |
| `defaults.dueDays` | number |  |
| `defaults.itemType` | string |  |
| `defaults.itemTypeId` | string |  |
| `defaults.notes` | string |  |
| `defaults.subject` | string |  |
| `defaults.tax` | number |  |
| `defaults.tax2` | number |  |
| `defaults.tax2Percent` | number |  |
| `defaults.taxPercent` | number |  |
| `defaults.taxType` | string |  |
| `exportFields` | object |  |
| `exportFields.itemType` | boolean |  |
| `exportFields.quantity` | boolean |  |
| `exportFields.rtl` | boolean |  |
| `exportFields.tax` | boolean |  |
| `exportFields.tax2` | boolean |  |
| `exportFields.unitPrice` | boolean |  |
| `labels` | object |  |
| `labels.amount` | string |  |
| `labels.billFrom` | string |  |
| `labels.billTo` | string |  |
| `labels.description` | string |  |
| `labels.discount` | string |  |
| `labels.dueDate` | string |  |
| `labels.issueDate` | string |  |
| `labels.itemType` | string |  |
| `labels.notes` | string |  |
| `labels.paid` | string |  |
| `labels.quantity` | string |  |
| `labels.subtotal` | string |  |
| `labels.tax` | string |  |
| `labels.tax2` | string |  |
| `labels.total` | string |  |
| `labels.totalAmount` | string |  |
| `labels.unitPrice` | string |  |

## Native endpoint

Through the native Clockify API, this operation is `PUT workspaces/:workspaceId/invoices/settings` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-invoice-settings.md) for the provider-specific parameters and requirements.

