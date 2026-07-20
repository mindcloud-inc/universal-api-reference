# GanttPRO: List Projects

Retrieves projects from your GanttPRO account.

```
GET https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-projects?${params}`, {
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
      "id": 1,
      "isArchived": 1,
      "lastUpdate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "projectId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `isArchived` | number |  |
| `lastUpdate` | date |  |
| `name` | string |  |
| `projectId` | number |  |

## Native endpoint

Through the native GanttPRO API, this operation is `GET /projects` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-projects.md) for the provider-specific parameters and requirements.

