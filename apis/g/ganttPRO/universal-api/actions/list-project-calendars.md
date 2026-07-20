# GanttPRO: List Project Calendars

Retrieves project calendars from your GanttPRO account.

```
GET https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-project-calendars
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-project-calendars?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/list-project-calendars?${params}`, {
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
      "customDays": [
        {}
      ],
      "projectId": 1,
      "worktime": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customDays` | array<object> |  |
| `projectId` | number |  |
| `worktime` | object |  |

## Native endpoint

Through the native GanttPRO API, this operation is `GET /projects/calendars` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-project-calendars.md) for the provider-specific parameters and requirements.

