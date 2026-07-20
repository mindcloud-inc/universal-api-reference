# pretix: List Events

Retrieves events from a pretix organizer.

```
GET https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a pretix `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0&organizer=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "organizer": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pretix/latest/actions/list-events?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "dateAdmission": "string",
      "dateFrom": "string",
      "dateTo": "string",
      "hasSubevents": true,
      "isPublic": true,
      "live": true,
      "name": {},
      "plugins": [
        "string"
      ],
      "publicUrl": "https://example.com",
      "slug": "string",
      "testmode": true,
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `dateAdmission` | string |  |
| `dateFrom` | string |  |
| `dateTo` | string |  |
| `hasSubevents` | boolean |  |
| `isPublic` | boolean |  |
| `live` | boolean |  |
| `name` | object |  |
| `plugins[]` | string |  |
| `publicUrl` | string |  |
| `slug` | string |  |
| `testmode` | boolean |  |
| `timezone` | string |  |

## Native endpoint

Through the native pretix API, this operation is `GET /organizers/:organizer/events/` (base URL `https://pretix.eu/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

