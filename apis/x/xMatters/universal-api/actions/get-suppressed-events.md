# xMatters: Get suppressed events

Retrieves suppressed events from your xMatters instance.

```
GET https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-suppressed-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a xMatters `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-suppressed-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/xMatters/latest/actions/get-suppressed-events?${params}`, {
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
| `event` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "data": [
        {
          "event": {
            "eventId": "string",
            "id": "string",
            "links": {
              "self": "https://example.com"
            }
          },
          "links": {
            "self": "https://example.com"
          },
          "match": {
            "at": "2026-05-07T12:00:00.000Z",
            "eventId": "string",
            "filters": [
              {
                "id": "string",
                "name": "Ava Chen"
              }
            ],
            "id": "string",
            "links": {
              "self": "https://example.com"
            }
          }
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `data[].event.eventId` | string |  |
| `data[].event.id` | string |  |
| `data[].event.links.self` | string |  |
| `data[].links.self` | string |  |
| `data[].match.at` | date |  |
| `data[].match.eventId` | string |  |
| `data[].match.filters[].id` | string |  |
| `data[].match.filters[].name` | string |  |
| `data[].match.id` | string |  |
| `data[].match.links.self` | string |  |
| `total` | number |  |

## Native endpoint

Through the native xMatters API, this operation is `GET event-suppressions` (base URL `https://mindcloud.xmatters.com/api/xm/1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-suppressed-events.md) for the provider-specific parameters and requirements.

