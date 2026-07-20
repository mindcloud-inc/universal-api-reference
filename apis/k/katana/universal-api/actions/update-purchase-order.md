# Katana: Update Purchase Order

Updates an existing purchase order in Katana.

```
PUT https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-purchase-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Katana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-purchase-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/katana/latest/actions/update-purchase-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Purchase order id |
| `orderNo` | string | no | Updatable only when status is in DRAFT, NOT_RECEIVED and PARTIALLY_RECEIVED |
| `supplierId` | number | no | Updatable only when status is in DRAFT and NOT_RECEIVED |
| `currency` | string | no | Updatable only when status is in DRAFT and NOT_RECEIVED |
| `trackingLocationId` | string | no | Updatable only when status is in DRAFT and NOT_RECEIVED and entity_type is outsourced |
| `status` | string | no |  |
| `expectedArrivalDate` | string | no | Updatable only when status is in DRAFT, NOT_RECEIVED and PARTIALLY_RECEIVED. Update will override arrival_date on purchase order rows |
| `orderCreatedDate` | string | no |  |
| `locationId` | number | no | Updatable only when status is in DRAFT and NOT_RECEIVED |
| `additionalInfo` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "additionalInfo": "string",
      "billingStatus": "string",
      "createdAt": "string",
      "currency": "string",
      "defaultGroupId": 1,
      "deletedAt": "string",
      "entityType": "string",
      "expectedArrivalDate": "string",
      "id": 1,
      "lastDocumentStatus": "string",
      "locationId": 1,
      "orderCreatedDate": "string",
      "orderNo": "string",
      "status": "string",
      "supplierId": 1,
      "total": 1,
      "totalInBaseCurrency": 1,
      "trackingLocationId": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additionalInfo` | string |  |
| `billingStatus` | string |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `defaultGroupId` | number |  |
| `deletedAt` | string |  |
| `entityType` | string |  |
| `expectedArrivalDate` | string |  |
| `id` | number |  |
| `lastDocumentStatus` | string |  |
| `locationId` | number |  |
| `orderCreatedDate` | string |  |
| `orderNo` | string |  |
| `status` | string |  |
| `supplierId` | number |  |
| `total` | number |  |
| `totalInBaseCurrency` | number |  |
| `trackingLocationId` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Katana API, this operation is `PATCH /purchase_orders/:id` (base URL `https://api.katanamrp.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-purchase-order.md) for the provider-specific parameters and requirements.

