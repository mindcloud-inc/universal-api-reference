# Clockify: Get Invoice Settings

Retrieves workspace invoice settings from Clockify.

```
GET https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-invoice-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-invoice-settings?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clockify/latest/actions/get-invoice-settings?${params}`, {
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
| `workspaceId` | list<string> | yes |  |

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

Through the native Clockify API, this operation is `GET workspaces/:workspaceId/invoices/settings` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-settings.md) for the provider-specific parameters and requirements.

