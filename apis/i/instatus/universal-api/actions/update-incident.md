# Instatus: Update Incident



```
PUT https://connect.mindcloud.co/v1/universal/instatus/latest/actions/update-incident
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/update-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "incidentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instatus/latest/actions/update-incident', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "incidentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Incident name. |
| `pageId` | string | yes | Instatus status page ID. |
| `status` | string | no | Incident status. |
| `incidentId` | string | yes | Instatus incident ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "components": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "id": "string",
      "impact": "string",
      "message": "string",
      "messageHtml": "string",
      "name": "Ava Chen",
      "resolved": "2026-05-07T12:00:00.000Z",
      "started": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updates": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `components` | array<object> |  |
| `createdAt` | date |  |
| `duration` | number |  |
| `id` | string |  |
| `impact` | string |  |
| `message` | string |  |
| `messageHtml` | string |  |
| `name` | string |  |
| `resolved` | date |  |
| `started` | date |  |
| `status` | string |  |
| `updatedAt` | date |  |
| `updates` | array<object> |  |

## Native endpoint

Through the native Instatus API, this operation is `PUT /v1/:page_id/incidents/:incident_id` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-incident.md) for the provider-specific parameters and requirements.

