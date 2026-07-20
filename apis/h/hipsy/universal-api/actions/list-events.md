# Hipsy: List Events

Retrieves events from a Hipsy organisation.

```
GET https://connect.mindcloud.co/v1/universal/hipsy/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hipsy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hipsy/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0&organisationSlug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organisationSlug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hipsy/latest/actions/list-events?${params}`, {
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
| `organisationSlug` | string | yes | Slug of the organisation whose events should be listed. |
| `period` | list | no | Which events to return: upcoming, past, or all. One of: `all`, `past`, `upcoming`. Default: `upcoming`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "date_until": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "latitude": "string",
      "location": "string",
      "longitude": "string",
      "picture": "string",
      "picture_small": "string",
      "qr_ticketshop": "string",
      "tickets": [
        {}
      ],
      "title": "string",
      "url_hipsy": "https://example.com",
      "url_ticketshop": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Start date and time of the event. |
| `date_until` | date | End date and time of the event. |
| `id` | number | The ID of the event. |
| `latitude` | string | The latitude of the event location. |
| `location` | string | The location of the event. |
| `longitude` | string | The longitude of the event location. |
| `picture` | string | URL of the event picture. |
| `picture_small` | string | URL of the smaller event picture. |
| `qr_ticketshop` | string | QR image URL for the ticket shop. |
| `tickets` | array<object> | Configured tickets for the event. |
| `title` | string | The title of the event. |
| `url_hipsy` | string | URL of the event page on Hipsy. |
| `url_ticketshop` | string | URL of the ticket shop for the event. |

## Native endpoint

Through the native Hipsy API, this operation is `GET /organisation/:organisationSlug/events` (base URL `https://api.hipsy.nl/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

