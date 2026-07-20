# Evenium: List Guest Accommodations

Retrieves guest accommodations from Evenium.

```
GET https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-guest-accommodations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Evenium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-guest-accommodations?connectionId=$CONNECTION_ID&contactId=1&eventId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1",
  "eventId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/evenium/latest/actions/list-guest-accommodations?${params}`, {
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
| `contactId` | number | yes | The Evenium Contact ID. |
| `eventId` | number | yes | The Evenium Event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checkinDate": "2026-05-07T12:00:00.000Z",
      "checkoutDate": "2026-05-07T12:00:00.000Z",
      "roomId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checkinDate` | date | Accommodation check-in date. |
| `checkoutDate` | date | Accommodation check-out date. |
| `roomId` | number | Booked room ID. |
| `status` | string | Accommodation status. |

## Native endpoint

Through the native Evenium API, this operation is `GET /events/:eventId/guests/:contactId/accommodations` (base URL `https://evenium.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-guest-accommodations.md) for the provider-specific parameters and requirements.

