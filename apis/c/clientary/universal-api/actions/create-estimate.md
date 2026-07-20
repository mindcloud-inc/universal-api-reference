# Clientary: Create Estimate

Creates a new estimate in Clientary.

```
POST https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clientary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "estimate.currencyCode": "string",
  "estimate.date": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clientary/latest/actions/create-estimate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "estimate.currencyCode": "string",
    "estimate.date": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `estimate.currencyCode` | string | yes | The ISO currency code for the estimate. |
| `estimate.date` | string | yes | The estimate issue date (YYYY-MM-DD). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowReincrement": true,
      "attachmentCurrentPage": 1,
      "attachments": [
        {}
      ],
      "attachmentsEnabled": true,
      "attachmentsRelations": [
        {}
      ],
      "attachmentTotalCount": 1,
      "attachmentTotalPages": 1,
      "clientId": 1,
      "clientViewUrl": "https://example.com",
      "comments": [
        {}
      ],
      "compoundTax": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currencyCode": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "deliveryDate": "2026-05-07T12:00:00.000Z",
      "estimateItems": [
        {}
      ],
      "expirationDate": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "note": "string",
      "number": "string",
      "po": "string",
      "recipients": [
        {}
      ],
      "scope": "string",
      "secret": "string",
      "shippingAddress": "string",
      "shippingCity": "string",
      "shippingCountry": "string",
      "shippingEnabled": true,
      "shippingName": "Ava Chen",
      "shippingPhone": "string",
      "shippingState": "string",
      "shippingZip": "string",
      "showTotals": true,
      "showUnits": true,
      "sortTimestamp": "2026-05-07T12:00:00.000Z",
      "status": 1,
      "subtotal": 1,
      "tax": 1,
      "tax2": 1,
      "tax2Enabled": true,
      "tax2Label": "string",
      "tax3": 1,
      "tax3Label": "string",
      "taxLabel": "string",
      "title": "string",
      "totalCost": 1,
      "totalTax": 1,
      "totalTax2": 1,
      "totalTax3": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowReincrement` | boolean |  |
| `attachmentCurrentPage` | number |  |
| `attachments` | array<object> |  |
| `attachmentsEnabled` | boolean |  |
| `attachmentsRelations` | array<object> |  |
| `attachmentTotalCount` | number |  |
| `attachmentTotalPages` | number |  |
| `clientId` | number |  |
| `clientViewUrl` | string |  |
| `comments` | array<object> |  |
| `compoundTax` | boolean |  |
| `createdAt` | date |  |
| `currencyCode` | string |  |
| `date` | date |  |
| `deliveryDate` | date |  |
| `estimateItems` | array<object> |  |
| `expirationDate` | date |  |
| `id` | number |  |
| `note` | string |  |
| `number` | string |  |
| `po` | string |  |
| `recipients` | array<object> |  |
| `scope` | string |  |
| `secret` | string |  |
| `shippingAddress` | string |  |
| `shippingCity` | string |  |
| `shippingCountry` | string |  |
| `shippingEnabled` | boolean |  |
| `shippingName` | string |  |
| `shippingPhone` | string |  |
| `shippingState` | string |  |
| `shippingZip` | string |  |
| `showTotals` | boolean |  |
| `showUnits` | boolean |  |
| `sortTimestamp` | date |  |
| `status` | number |  |
| `subtotal` | number |  |
| `tax` | number |  |
| `tax2` | number |  |
| `tax2Enabled` | boolean |  |
| `tax2Label` | string |  |
| `tax3` | number |  |
| `tax3Label` | string |  |
| `taxLabel` | string |  |
| `title` | string |  |
| `totalCost` | number |  |
| `totalTax` | number |  |
| `totalTax2` | number |  |
| `totalTax3` | number |  |
| `updatedAt` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native Clientary API, this operation is `POST /estimates` (base URL `https://{{credentials.subdomain}}.clientary.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-estimate.md) for the provider-specific parameters and requirements.

