# Sprintful: List Bookings

Retrieves booking events available in Sprintful.

```
GET https://connect.mindcloud.co/v1/universal/sprintful/latest/actions/list-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sprintful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sprintful/latest/actions/list-bookings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sprintful/latest/actions/list-bookings?${params}`, {
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
| `limit` | string | no | Maximum number of bookings to return. Sprintful defaults to 50. |
| `offset` | string | no | Number of bookings to skip before returning results. |
| `startDate` | string | no | Filter bookings starting on or after this date. Sprintful format: DD-MM-YYY. |
| `endDate` | string | no | Filter bookings ending on or before this date. Sprintful format: DD-MM-YYY. |
| `pageSlug` | string | no | Only return bookings for a specific page slug. |
| `excludePageSlug` | string | no | Exclude bookings for a specific page slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "appointmentName": "Ava Chen",
        "createdAt": "string",
        "end": "string",
        "form": [
          {}
        ],
        "id": "string",
        "location": "string",
        "pageSlug": "string",
        "pageUrl": "https://example.com",
        "start": "string",
        "subPageNames": [
          "Ava Chen"
        ],
        "subPageSlugs": [
          "string"
        ],
        "url": "https://example.com",
        "visitorEmail": "ava@example.com",
        "visitorName": "Ava Chen",
        "visitorTimezone": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Bookings returned by Sprintful. |
| `data.appointmentName` | string | Appointment name. |
| `data.createdAt` | string | Booking creation timestamp. |
| `data.end` | string | Booking end timestamp. |
| `data.form` | array<object> | Booking form submission values. |
| `data.id` | string | The booking identifier. |
| `data.location` | string | Appointment location. |
| `data.pageSlug` | string | The associated booking page slug. |
| `data.pageUrl` | string | The associated booking page URL. |
| `data.start` | string | Booking start timestamp. |
| `data.subPageNames` | array<string> | Assigned sub-page names for team bookings. |
| `data.subPageSlugs` | array<string> | Assigned sub-page slugs for team bookings. |
| `data.url` | string | The booking URL. |
| `data.visitorEmail` | string | Visitor email. |
| `data.visitorName` | string | Visitor name. |
| `data.visitorTimezone` | string | Visitor timezone. |
| `success` | boolean | Whether the Sprintful request succeeded. |

## Native endpoint

Through the native Sprintful API, this operation is `GET /bookings` (base URL `https://app.sprintful.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bookings.md) for the provider-specific parameters and requirements.

