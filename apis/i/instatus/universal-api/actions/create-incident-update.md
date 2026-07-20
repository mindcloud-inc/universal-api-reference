# Instatus: Create Incident Update



```
POST https://connect.mindcloud.co/v1/universal/instatus/latest/actions/create-incident-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/create-incident-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "status": "string",
  "incidentId": "string",
  "components[]": [
    "string"
  ],
  "statuses[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instatus/latest/actions/create-incident-update', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "status": "string",
    "incidentId": "string",
    "components[]": ["string"],
    "statuses[]": [{}]
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
| `status` | string | yes | Incident update status. |
| `incidentId` | string | yes | Instatus incident ID. |
| `components[]` | array<string> | yes | Affected component IDs. Accepts multiple values as an array. |
| `notify` | boolean | no | Whether to notify subscribers. Default: `false`. |
| `statuses[]` | array<object> | yes | Statuses for each affected component. Include matching component IDs in Component IDs. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "ended": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "incidentId": "string",
      "message": "string",
      "messageHtml": "string",
      "notify": true,
      "started": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `duration` | number |  |
| `ended` | date |  |
| `id` | string |  |
| `incidentId` | string |  |
| `message` | string |  |
| `messageHtml` | string |  |
| `notify` | boolean |  |
| `started` | date |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Instatus API, this operation is `POST /v1/:page_id/incidents/:incident_id/incident-updates` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-incident-update.md) for the provider-specific parameters and requirements.

