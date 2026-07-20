# pretix: Get Check In List

Retrieves a check-in list from pretix.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-check-in-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-check-in-list?connectionId=$CONNECTION_ID&organizer=string&event=string&list=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizer": "string",
  "event": "string",
  "list": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/get-check-in-list?${params}`, {
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
| `list` | string | yes | pretix check-in list ID. |

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

Through the native pretix API, this operation is `GET /organizers/:organizer/events/:event/checkinlists/:list/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-check-in-list.md) for the provider-specific parameters and requirements.

