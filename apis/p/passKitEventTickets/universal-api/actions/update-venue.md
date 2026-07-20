# PassKit Event Tickets: Update Venue

Fully updates an existing venue in PassKit.

```
PUT https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/update-venue
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PassKit Event Tickets `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/update-venue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/passKitEventTickets/latest/actions/update-venue', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "countryCode": "string",
      "id": "string",
      "name": "Ava Chen",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `countryCode` | string |  |
| `id` | string |  |
| `name` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native PassKit Event Tickets API, this operation is `PUT /eventTickets/venue` (base URL `https://api.pub2.passkit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-venue.md) for the provider-specific parameters and requirements.

