# Checkout Page: Create Ticket Type

Creates a ticket type in Checkout Page.

```
POST https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/create-ticket-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/create-ticket-type" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "ticketGroupId": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/create-ticket-type', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "ticketGroupId": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageId` | string | yes | The unique identifier of the page. |
| `ticketGroupId` | string | yes | The unique identifier of the ticket group. |
| `name` | string | yes | Name of the ticket type. |
| `description` | string | no | Description of the ticket type. |
| `status` | string | no | Status of the ticket type. Defaults to `enabled`. |
| `price` | number | no | Price in smallest currency unit (cents). Defaults to `0`. |
| `reference` | string | no | External reference ID for the ticket type. |
| `hidden` | boolean | no | Whether the ticket type is hidden from customers. |
| `hideWhenSoldOut` | boolean | no | Hide the ticket type when sold out. |
| `hideWhenNotOnSale` | boolean | no | Hide the ticket type when not on sale. |
| `hideWhenScheduled` | boolean | no | Hide the ticket type when scheduled for future sale. |
| `hideWhenUnavailable` | boolean | no | Hide the ticket type when unavailable. |
| `pricing` | string | no | Pricing type for the ticket. Defaults to `paid`. |
| `discountedFromPrice` | number | no | Original price to show as discounted from (strike-through price). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availabilityBehavior": "string",
      "availabilityStatus": "string",
      "capacity": 1,
      "description": "string",
      "discountedFromPrice": 1,
      "hidden": true,
      "hideWhenNotOnSale": true,
      "hideWhenScheduled": true,
      "hideWhenSoldOut": true,
      "hideWhenUnavailable": true,
      "id": "string",
      "image": {},
      "maxQuantity": 1,
      "minQuantity": 1,
      "name": "Ava Chen",
      "price": 1,
      "pricing": "string",
      "quantitySold": 1,
      "reference": "string",
      "saleEndOn": "string",
      "saleStartOn": "string",
      "showAvailableQuantity": true,
      "showTicketSaleDates": true,
      "status": "string",
      "ticketGroupId": "string",
      "triggerTicketTypeId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availabilityBehavior` | string | Controls when the ticket becomes available for purchase. |
| `availabilityStatus` | string | Current availability status. |
| `capacity` | number | Maximum tickets available. Null means unlimited. |
| `description` | string | Description of the ticket type. |
| `discountedFromPrice` | number | Strike-through price in smallest currency unit. |
| `hidden` | boolean | Whether the ticket type is hidden from customers. |
| `hideWhenNotOnSale` | boolean | Whether hidden when not on sale. |
| `hideWhenScheduled` | boolean | Whether hidden when scheduled for future sale. |
| `hideWhenSoldOut` | boolean | Whether hidden when sold out. |
| `hideWhenUnavailable` | boolean | Whether hidden when unavailable. |
| `id` | string | Unique identifier for the ticket type. |
| `image` | object | Image for the ticket type. |
| `maxQuantity` | number | Maximum tickets per order. |
| `minQuantity` | number | Minimum tickets required per order. |
| `name` | string | Name of the ticket type. |
| `price` | number | Price in smallest currency unit (e.g. cents). |
| `pricing` | string | Pricing type. |
| `quantitySold` | number | Number of tickets sold. |
| `reference` | string | External reference ID. |
| `saleEndOn` | string | Sale end date in ISO 8601 format. |
| `saleStartOn` | string | Sale start date in ISO 8601 format. |
| `showAvailableQuantity` | boolean | Whether available quantity is shown to customers. |
| `showTicketSaleDates` | boolean | Whether sale start/end dates are shown to customers. |
| `status` | string | Status of the ticket type. |
| `ticketGroupId` | string | ID of the ticket group this ticket type belongs to. This moves the ticket from the current group to the new group. |
| `triggerTicketTypeId` | string | ID of the ticket type that triggers this ticket type to become available. |

## Native endpoint

Through the native Checkout Page API, this operation is `POST /v1/events/:pageId/ticket-groups/:ticketGroupId/ticket-types` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-ticket-type.md) for the provider-specific parameters and requirements.

