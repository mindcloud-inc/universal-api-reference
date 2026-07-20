# Instatus: Create Maintenance



```
POST https://connect.mindcloud.co/v1/universal/instatus/latest/actions/create-maintenance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/create-maintenance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "pageId": "string",
  "start": "string",
  "end": "string",
  "status": "string",
  "notify": "false",
  "components[]": [
    "string"
  ],
  "autoStart": "false",
  "autoEnd": "false",
  "notifyStart": "false",
  "notifyEnd": "false",
  "notifyEarly": "false"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instatus/latest/actions/create-maintenance', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "pageId": "string",
    "start": "string",
    "end": "string",
    "status": "string",
    "notify": "false",
    "components[]": ["string"],
    "autoStart": "false",
    "autoEnd": "false",
    "notifyStart": "false",
    "notifyEnd": "false",
    "notifyEarly": "false"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Maintenance name. |
| `pageId` | string | yes | Instatus status page ID. |
| `message` | string | no | Maintenance message. |
| `start` | string | yes | Maintenance start time. |
| `end` | string | yes | Maintenance end time. |
| `status` | string | yes | Maintenance status, such as NOTSTARTEDYET, INPROGRESS, or COMPLETED. |
| `notify` | boolean | yes | Whether to notify subscribers. Default: `false`. |
| `components[]` | array<string> | yes | Affected component IDs. Accepts multiple values as an array. |
| `autoStart` | boolean | yes | Whether Instatus should automatically start the maintenance at the start time. Default: `false`. |
| `autoEnd` | boolean | yes | Whether Instatus should automatically end the maintenance at the end time. Default: `false`. |
| `notifyStart` | boolean | yes | Whether to notify subscribers when maintenance starts. Default: `false`. |
| `notifyEnd` | boolean | yes | Whether to notify subscribers when maintenance ends. Default: `false`. |
| `notifyEarly` | boolean | yes | Whether to notify subscribers before maintenance starts. Default: `false`. |
| `duration` | number | no | Maintenance duration in minutes. Default: `60`. |
| `statuses[]` | array<object> | no | Statuses for each affected component. Include matching component IDs in Component IDs. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoEnd": true,
      "autoStart": true,
      "components": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "end": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "impact": "string",
      "message": "string",
      "messageHtml": "string",
      "name": "Ava Chen",
      "notify": true,
      "notifyEarly": true,
      "notifyEnd": true,
      "notifyStart": true,
      "siteId": "string",
      "start": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "translations": {},
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
| `autoEnd` | boolean |  |
| `autoStart` | boolean |  |
| `components` | array<object> |  |
| `createdAt` | date |  |
| `duration` | number |  |
| `end` | date |  |
| `id` | string |  |
| `impact` | string |  |
| `message` | string |  |
| `messageHtml` | string |  |
| `name` | string |  |
| `notify` | boolean |  |
| `notifyEarly` | boolean |  |
| `notifyEnd` | boolean |  |
| `notifyStart` | boolean |  |
| `siteId` | string |  |
| `start` | date |  |
| `status` | string |  |
| `translations` | object |  |
| `updatedAt` | date |  |
| `updates` | array<object> |  |

## Native endpoint

Through the native Instatus API, this operation is `POST /v1/:page_id/maintenances` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-maintenance.md) for the provider-specific parameters and requirements.

