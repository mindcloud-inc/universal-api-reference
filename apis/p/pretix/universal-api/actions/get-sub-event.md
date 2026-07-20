# pretix: Get Sub Event

Retrieves a sub-event from pretix.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-sub-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-sub-event?connectionId=$CONNECTION_ID&organizer=string&event=string&subevent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizer": "string",
  "event": "string",
  "subevent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-sub-event?${params}`, {
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
| `organizer` | string | yes | pretix organizer slug. |
| `event` | string | yes | pretix event slug. |
| `subevent` | string | yes | pretix sub-event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "dateAdmission": "string",
      "dateFrom": "string",
      "dateTo": "string",
      "event": "string",
      "frontpageText": {},
      "geoLat": 1,
      "geoLon": 1,
      "id": 1,
      "isPublic": true,
      "location": {},
      "name": {},
      "presaleEnd": "string",
      "presaleStart": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `dateAdmission` | string |  |
| `dateFrom` | string |  |
| `dateTo` | string |  |
| `event` | string |  |
| `frontpageText` | object |  |
| `geoLat` | number |  |
| `geoLon` | number |  |
| `id` | number |  |
| `isPublic` | boolean |  |
| `location` | object |  |
| `name` | object |  |
| `presaleEnd` | string |  |
| `presaleStart` | string |  |

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/events/:event/subevents/:subevent/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sub-event.md) for the provider-specific parameters and requirements.

