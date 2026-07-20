# Leadspicker: List Project Timeline Events

Retrieves timeline events for a project in Leadspicker.

```
GET https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-project-timeline-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leadspicker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-project-timeline-events?connectionId=$CONNECTION_ID&projectId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leadspicker/latest/actions/list-project-timeline-events?${params}`, {
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
| `projectId` | number | yes | Leadspicker project identifier. |
| `page` | number | no | Page number for timeline events. Default: `1`. |
| `pageSize` | number | no | Number of timeline events per page. Default: `50`. |
| `search` | string | no | Search project timeline events. |
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

Through the native Leadspicker API, this operation is `GET /app/sb/api/projects/:project_id/events` (base URL `https://app.leadspicker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-timeline-events.md) for the provider-specific parameters and requirements.

