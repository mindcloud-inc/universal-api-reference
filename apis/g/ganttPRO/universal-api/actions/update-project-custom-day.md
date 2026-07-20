# GanttPRO: Update Project Custom Day

Updates a custom day in a GanttPRO project calendar.

```
PUT https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/update-project-custom-day
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GanttPRO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/update-project-custom-day" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customDayId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ganttPRO/latest/actions/update-project-custom-day', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customDayId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customDayId` | number | yes | GanttPRO custom day identifier. |
| `from` | string | no | Updated start date in YYYY-MM-DD format. Example: `YYYY-MM-DD`. |
| `to` | string | no | Updated end date in YYYY-MM-DD format. Example: `YYYY-MM-DD`. |
| `title` | string | no | Updated custom day title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string |  |

## Native endpoint

Through the native GanttPRO API, this operation is `PUT /projects/customday/:customDayId` (base URL `https://api.ganttpro.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project-custom-day.md) for the provider-specific parameters and requirements.

