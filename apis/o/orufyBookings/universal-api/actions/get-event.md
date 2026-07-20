# Orufy Bookings: Get Event



```
GET https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Orufy Bookings `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/get-event?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/orufyBookings/latest/actions/get-event?${params}`, {
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
| `eventId` | string | yes | The Orufy event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appInfo": {},
      "event": {},
      "isSuccess": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appInfo` | object | Orufy app metadata returned with the event. |
| `event` | object | The requested Orufy event. |
| `isSuccess` | boolean | Whether the request succeeded. |

## Native endpoint

Through the native Orufy Bookings API, this operation is `GET /api/event/:eventId` (base URL `https://bookings.orufy.com/api/v1/bookings`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

