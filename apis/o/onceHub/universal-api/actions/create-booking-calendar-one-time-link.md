# OnceHub: Create Booking Calendar One-Time Link



```
POST https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/create-booking-calendar-one-time-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OnceHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/create-booking-calendar-one-time-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onceHub/latest/actions/create-booking-calendar-one-time-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The OnceHub booking calendar identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creationTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creationTime` | date |  |
| `id` | string |  |
| `url` | string |  |

## Native endpoint

Through the native OnceHub API, this operation is `POST /v2/booking-calendars/:id/one-time-links` (base URL `https://api.oncehub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-booking-calendar-one-time-link.md) for the provider-specific parameters and requirements.

