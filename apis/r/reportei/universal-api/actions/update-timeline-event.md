# Reportei: Update Timeline Event

Updates an existing timeline event in Reportei.

```
PUT https://connect.mindcloud.co/v1/universal/reportei/latest/actions/update-timeline-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reportei `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/reportei/latest/actions/update-timeline-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "projectId": 1,
  "title": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/reportei/latest/actions/update-timeline-event', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "projectId": 1,
    "title": "string",
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID do evento. |
| `projectId` | number | yes | ID do projeto. |
| `reportId` | number | no | ID do relatório. |
| `title` | string | yes | Título do evento. |
| `content` | string | yes | Conteúdo do evento. |

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

Through the native Reportei API, this operation is `PUT /timeline-events/:id` (base URL `https://app.reportei.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-timeline-event.md) for the provider-specific parameters and requirements.

