# Reportei: Get Timeline Event

Retrieves a timeline event from Reportei.

```
GET https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-timeline-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reportei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-timeline-event?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/reportei/latest/actions/get-timeline-event?${params}`, {
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
| `id` | number | yes | ID do evento. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "timeline_event": {
        "date": "string",
        "id": 1,
        "project_id": 1,
        "title": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `timeline_event.date` | string | Timeline event date |
| `timeline_event.id` | number | Timeline event identifier |
| `timeline_event.project_id` | number | Related project identifier |
| `timeline_event.title` | string | Timeline event title |

## Native endpoint

Through the native Reportei API, this operation is `GET /timeline-events/:id` (base URL `https://app.reportei.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-timeline-event.md) for the provider-specific parameters and requirements.

