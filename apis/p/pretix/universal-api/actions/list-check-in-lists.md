# pretix: List Check In Lists

Retrieves check-in lists from a pretix event.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-check-in-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-check-in-lists?connectionId=$CONNECTION_ID&limit=25&offset=0&organizer=string&event=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizer": "string",
  "event": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-check-in-lists?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowEntryAfterExit": true,
      "allowMultipleEntries": true,
      "allProducts": true,
      "checkinCount": 1,
      "exitAllAt": "string",
      "id": 1,
      "includePending": true,
      "limitProducts": [
        1
      ],
      "name": "Ava Chen",
      "positionCount": 1,
      "rules": {},
      "subevent": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowEntryAfterExit` | boolean |  |
| `allowMultipleEntries` | boolean |  |
| `allProducts` | boolean |  |
| `checkinCount` | number |  |
| `exitAllAt` | string |  |
| `id` | number |  |
| `includePending` | boolean |  |
| `limitProducts[]` | number |  |
| `name` | string |  |
| `positionCount` | number |  |
| `rules` | object |  |
| `subevent` | number |  |

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/events/:event/checkinlists/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-check-in-lists.md) for the provider-specific parameters and requirements.

