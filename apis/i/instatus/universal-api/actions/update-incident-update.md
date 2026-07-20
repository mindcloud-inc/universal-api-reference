# Instatus: Update Incident Update



```
PUT https://connect.mindcloud.co/v1/universal/instatus/latest/actions/update-incident-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/update-incident-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "incidentId": "string",
  "incidentUpdateId": "string",
  "started": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instatus/latest/actions/update-incident-update', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "incidentId": "string",
    "incidentUpdateId": "string",
    "started": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | no | Incident update message. |
| `pageId` | string | yes | Instatus status page ID. |
| `incidentId` | string | yes | Instatus incident ID. |
| `incidentUpdateId` | string | yes | Instatus incident update ID. |
| `started` | string | yes | Date and time when this incident update happened. |
| `status` | string | no | Incident update status. |
| `notify` | boolean | no | Whether to notify subscribers. Default: `false`. |
| `components[]` | array<string> | no | IDs of affected components. Accepts multiple values as an array. |
| `statuses[]` | array<object> | no | Statuses for each affected component. Include matching component IDs in Component IDs. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "ended": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "incident": {},
      "incidentId": "string",
      "message": "string",
      "messageHtml": "string",
      "notify": true,
      "started": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "translations": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> |  |
| `createdAt` | date |  |
| `duration` | number |  |
| `ended` | date |  |
| `id` | string |  |
| `incident` | object |  |
| `incidentId` | string |  |
| `message` | string |  |
| `messageHtml` | string |  |
| `notify` | boolean |  |
| `started` | date |  |
| `status` | string |  |
| `translations` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Instatus API, this operation is `PUT /v1/:page_id/incidents/:incident_id/incident-updates/:incident_update_id` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-incident-update.md) for the provider-specific parameters and requirements.

