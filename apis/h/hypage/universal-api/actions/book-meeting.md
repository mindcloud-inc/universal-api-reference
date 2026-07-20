# Hy.page: Book Meeting



```
POST https://connect.mindcloud.co/v1/universal/hypage/latest/actions/book-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hy.page `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hypage/latest/actions/book-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "slotId": "string",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hypage/latest/actions/book-meeting', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "slotId": "string",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `notes` | string | no | Booking notes. |
| `slotId` | string | yes | Meeting slot ID. |
| `email` | string | yes | Booker email address. |
| `name` | string | no | Booker name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bookingId": "string",
      "peopleId": "string",
      "product": {},
      "slot": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookingId` | string |  |
| `peopleId` | string |  |
| `product` | object |  |
| `slot` | object |  |
| `status` | string |  |

## Native endpoint

Through the native Hy.page API, this operation is `POST /hyax-api/v1/meetings/book` (base URL `https://platform.hyax.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/book-meeting.md) for the provider-specific parameters and requirements.

