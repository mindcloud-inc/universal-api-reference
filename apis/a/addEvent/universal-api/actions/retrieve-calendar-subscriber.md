# AddEvent: Retrieve calendar subscriber



```
GET https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/retrieve-calendar-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AddEvent `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/retrieve-calendar-subscriber?connectionId=$CONNECTION_ID&subscriberId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "subscriberId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/addEvent/latest/actions/retrieve-calendar-subscriber?${params}`, {
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
| `subscriberId` | string | yes | Unique identifier for the calendar subscriber. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "calendarId": "string",
      "calendarType": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "geoLocation": {
        "city": "string",
        "country": "string",
        "ip": "string",
        "location": "string",
        "postal": "string",
        "region": "string"
      },
      "id": "string",
      "subscriberStatus": "string",
      "syncCount": 1,
      "synced": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calendarId` | string | Associated calendar ID. |
| `calendarType` | string | Calendar service used by the subscriber. |
| `created` | date | Subscriber creation timestamp. |
| `geoLocation.city` | string |  |
| `geoLocation.country` | string |  |
| `geoLocation.ip` | string |  |
| `geoLocation.location` | string |  |
| `geoLocation.postal` | string |  |
| `geoLocation.region` | string |  |
| `id` | string | Unique identifier of the calendar subscriber. |
| `subscriberStatus` | string | Subscriber status. |
| `syncCount` | number | Number of feed syncs. |
| `synced` | date | Last feed sync timestamp. |

## Native endpoint

Through the native AddEvent API, this operation is `GET /subscribers/:subscriber_id` (base URL `https://api.addevent.com/calevent/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-calendar-subscriber.md) for the provider-specific parameters and requirements.

