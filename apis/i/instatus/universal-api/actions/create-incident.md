# Instatus: Create Incident



```
POST https://connect.mindcloud.co/v1/universal/instatus/latest/actions/create-incident
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/create-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instatus/latest/actions/create-incident', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | no | Initial incident message. |
| `name` | string | no | Incident name. |
| `pageId` | string | yes | Instatus status page ID. |
| `started` | string | no | Incident start time. |
| `status` | string | no | Incident status, such as INVESTIGATING, IDENTIFIED, MONITORING, or RESOLVED. |
| `components[]` | array<string> | no | Affected component IDs. Accepts multiple values as an array. |
| `notify` | boolean | no | Whether to notify subscribers. Default: `false`. |
| `shouldPublish` | boolean | no | Set false to create an unpublished incident. Default: `false`. |

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

Through the native Instatus API, this operation is `POST /v1/:page_id/incidents` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-incident.md) for the provider-specific parameters and requirements.

