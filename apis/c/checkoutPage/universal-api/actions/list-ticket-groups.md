# Checkout Page: List Ticket Groups

Retrieves ticket groups from Checkout Page.

```
GET https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-ticket-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkout Page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-ticket-groups?connectionId=$CONNECTION_ID&pageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkoutPage/latest/actions/list-ticket-groups?${params}`, {
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
| `pageId` | string | yes | The unique identifier of the event page. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "availabilityBehavior": "string",
      "availabilityStatus": "string",
      "bulkDiscounts": [
        {}
      ],
      "capacity": 1,
      "description": "string",
      "hidden": true,
      "hideWhenNotOnSale": true,
      "hideWhenScheduled": true,
      "hideWhenSoldOut": true,
      "hideWhenUnavailable": true,
      "id": "string",
      "layout": {},
      "name": "Ava Chen",
      "preselect": {},
      "reference": "string",
      "saleEndOn": "string",
      "saleStartOn": "string",
      "status": "string",
      "ticketSelectionType": "string",
      "ticketTypeIds": [
        "string"
      ],
      "triggerTicketGroupId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availabilityBehavior` | string | Controls when the ticket group becomes available. |
| `availabilityStatus` | string | Current availability status of the ticket group. |
| `bulkDiscounts` | array<object> | Bulk discount tiers. |
| `capacity` | number | Maximum tickets sold across all types in this group. Null means unlimited. |
| `description` | string | Description of the ticket group. |
| `hidden` | boolean | Whether the ticket group is hidden from customers. |
| `hideWhenNotOnSale` | boolean | Whether hidden when not on sale. |
| `hideWhenScheduled` | boolean | Whether hidden when scheduled for future sale. |
| `hideWhenSoldOut` | boolean | Whether hidden when sold out. |
| `hideWhenUnavailable` | boolean | Whether hidden when unavailable. |
| `id` | string | Unique identifier for the ticket group. |
| `layout` | object | Display layout configuration. |
| `name` | string | Name of the ticket group. |
| `preselect` | object | Preselection configuration. |
| `reference` | string | External reference ID. |
| `saleEndOn` | string | Sale end date in ISO 8601 format. |
| `saleStartOn` | string | Sale start date in ISO 8601 format. |
| `status` | string | Status of the ticket group. |
| `ticketSelectionType` | string | How customers can select tickets. |
| `ticketTypeIds` | array<string> |  |
| `triggerTicketGroupId` | string | ID of the ticket group that triggers this group to become available. |

## Native endpoint

Through the native Checkout Page API, this operation is `GET /v1/events/:pageId/ticket-groups` (base URL `https://api.checkoutpage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ticket-groups.md) for the provider-specific parameters and requirements.

