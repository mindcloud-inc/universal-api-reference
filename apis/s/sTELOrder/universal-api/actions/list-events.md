# STEL Order: List Events

Retrieves a list of events from STEL Order.

```
GET https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a STEL Order `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sTELOrder/latest/actions/list-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "all-day": true,
      "calendar-id": 1,
      "calendar-path": "string",
      "creator-id": 1,
      "creator-path": "string",
      "deleted": true,
      "end-date": "string",
      "event-state": "string",
      "event-type-id": 1,
      "event-type-path": "string",
      "id": 1,
      "path": "string",
      "start-date": "string",
      "subject": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `all-day` | boolean |  |
| `calendar-id` | number |  |
| `calendar-path` | string |  |
| `creator-id` | number |  |
| `creator-path` | string |  |
| `deleted` | boolean |  |
| `end-date` | string |  |
| `event-state` | string |  |
| `event-type-id` | number |  |
| `event-type-path` | string |  |
| `id` | number |  |
| `path` | string |  |
| `start-date` | string |  |
| `subject` | string |  |

## Native endpoint

Through the native STEL Order API, this operation is `GET /events` (base URL `https://app.stelorder.com/app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

