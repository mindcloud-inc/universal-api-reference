# PassKit Event Tickets: Bulk Delete Tickets

Deletes multiple tickets from PassKit.

```
DELETE https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/bulk-delete-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Event Tickets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/bulk-delete-tickets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/bulk-delete-tickets?${params}`, {
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
      "deletedCount": 1,
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | boolean |  |
| `deletedCount` | number |  |
| `message` | string |  |

## Native endpoint

Through the native PassKit Event Tickets API, this operation is `DELETE /eventTickets/bulk` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-delete-tickets.md) for the provider-specific parameters and requirements.

