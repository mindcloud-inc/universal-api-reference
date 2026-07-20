# Leadspicker: List Dashboard Timeline Events

Retrieves dashboard timeline events from Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-dashboard-timeline-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-dashboard-timeline-events?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-dashboard-timeline-events?${params}`, {
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
| `page` | number | no | Dashboard logs page number. Default: `1`. |
| `pageSize` | number | no | Dashboard logs page size. Default: `50`. |
| `search` | string | no | Search dashboard logs. |
| `eventTypes` | string<string> | no | Comma-separated event types to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "page": 1,
      "page_size": 1,
      "results": [
        {}
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
| `page` | number |  |
| `page_size` | number |  |
| `results` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native Leadspicker API, this operation is `GET /app/sb/api/dashboard/logs` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dashboard-timeline-events.md) for the provider-specific parameters and requirements.

