# PassKit Event Tickets: Delete Tickets By Order Number

Deletes tickets by order number from PassKit.

```
DELETE https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/delete-tickets-by-order-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Event Tickets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/delete-tickets-by-order-number?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/delete-tickets-by-order-number?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": true,
      "message": "string",
      "orderNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `message` | string |  |
| `orderNumber` | string |  |

## Native endpoint

Through the native PassKit Event Tickets API, this operation is `DELETE /eventTickets/orderNumber` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tickets-by-order-number.md) for the provider-specific parameters and requirements.

