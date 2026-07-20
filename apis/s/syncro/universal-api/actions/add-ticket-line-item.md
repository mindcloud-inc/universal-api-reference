# Syncro: Add Ticket Line Item

Creates a ticket line item in Syncro.

```
POST https://connect.mindcloud.co/v1/universal/syncro/latest/actions/add-ticket-line-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Syncro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/syncro/latest/actions/add-ticket-line-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "name": "Ava Chen",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/syncro/latest/actions/add-ticket-line-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "name": "Ava Chen",
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Syncro ticket ID. |
| `name` | string | yes |  |
| `upcCode` | string | no |  |
| `productId` | number | no |  |
| `description` | string | yes |  |
| `quantity` | number | no |  |
| `priceCost` | number | no |  |
| `priceRetail` | number | no |  |
| `taxable` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "converted": true,
      "costCents": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "position": 1,
      "priceCost": 1,
      "priceRetail": 1,
      "productId": 1,
      "quantity": "string",
      "retailCents": 1,
      "taxable": true,
      "ticketId": 1,
      "upcCode": "string",
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
| `converted` | boolean |  |
| `costCents` | number |  |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `position` | number |  |
| `priceCost` | number |  |
| `priceRetail` | number |  |
| `productId` | number |  |
| `quantity` | string |  |
| `retailCents` | number |  |
| `taxable` | boolean |  |
| `ticketId` | number |  |
| `upcCode` | string |  |
| `updatedAt` | date |  |
| `userId` | number |  |

## Native endpoint

Through the native Syncro API, this operation is `POST /tickets/:id/add_line_item` (base URL `https://mindcloud.syncromsp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-ticket-line-item.md) for the provider-specific parameters and requirements.

