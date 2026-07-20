# Lettr: List Delivery Events



```
GET https://connect.mindcloud.co/v1/universal/lettr/latest/actions/list-delivery-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/list-delivery-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lettr/latest/actions/list-delivery-events?${params}`, {
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
      "data": {
        "events": {
          "data": [
            {}
          ],
          "from": "2026-05-07T12:00:00.000Z",
          "pagination": {
            "next_cursor": "string",
            "per_page": 1
          },
          "to": "2026-05-07T12:00:00.000Z",
          "total_count": 1
        }
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Email event list payload. |
| `data.events` | object | Event collection wrapper. |
| `data.events.data` | array<object> | Email events in the selected time range. |
| `data.events.from` | date | Range start timestamp. |
| `data.events.pagination` | object | Cursor pagination metadata. |
| `data.events.pagination.next_cursor` | string | Cursor for the next page when available. |
| `data.events.pagination.per_page` | number | Requested page size. |
| `data.events.to` | date | Range end timestamp. |
| `data.events.total_count` | number | Total event count for the query. |
| `message` | string | Email event list status message. |

## Native endpoint

Through the native Lettr API, this operation is `GET /emails/events` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-delivery-events.md) for the provider-specific parameters and requirements.

