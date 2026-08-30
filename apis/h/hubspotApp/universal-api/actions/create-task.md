# HubSpot: Create Task



```
POST https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HubSpot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "properties": {},
  "properties.hs_timestamp": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hubspotApp/latest/actions/create-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "properties": {},
    "properties.hs_timestamp": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `properties` | object | yes |  |
| `properties.hs_timestamp` | date | yes |  |
| `properties.hs_task_subject` | string | no |  |
| `properties.hs_task_body` | string | no |  |
| `properties.hubspot_owner_id` | string | no |  |
| `properties.hs_task_status` | string | no |  |
| `properties.hs_task_priority` | string | no |  |
| `properties.hs_task_type` | string | no |  |
| `properties.hs_task_reminders` | string | no |  |
| `associations[]` | array<object> | no |  |
| `associations[].to` | object | no |  |
| `associations[].to.id` | string | no |  |
| `associations[].types[]` | array<object> | no |  |
| `associations[].types[].associationCategory` | string | no |  |
| `associations[].types[].associationTypeId` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "properties": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the task is archived. |
| `archivedAt` | date | When the task was archived. |
| `createdAt` | date | When the task was created. |
| `id` | string | HubSpot task record ID. |
| `properties` | object | Task property values returned by HubSpot. |
| `updatedAt` | date | When the task was last updated. |
| `url` | string | HubSpot task record URL. |

## Native endpoint

Through the native HubSpot API, this operation is `POST crm/objects/2026-03/tasks` (base URL `https://api.hubapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-task.md) for the provider-specific parameters and requirements.

