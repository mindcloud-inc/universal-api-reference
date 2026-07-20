# Bokun: List Experience Booking Notes

Retrieves notes for an experience booking from Bokun.

```
GET https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-booking-notes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bokun `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-booking-notes?connectionId=$CONNECTION_ID&experienceBookingId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "experienceBookingId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bokun/latest/actions/list-experience-booking-notes?${params}`, {
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
| `experienceBookingId` | number | yes | The Bokun experience booking ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "owner_id": 1,
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `owner_id` | number |  |
| `text` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Bokun API, this operation is `GET /restapi/v2.0/experienceBooking/:experienceBookingId/notes` (base URL `https://api.bokun.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-experience-booking-notes.md) for the provider-specific parameters and requirements.

