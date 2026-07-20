# Instatus: Update Maintenance



```
PUT https://connect.mindcloud.co/v1/universal/instatus/latest/actions/update-maintenance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instatus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/update-maintenance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "maintenanceId": "string",
  "message": "string",
  "start": "string",
  "end": "string",
  "status": "string",
  "notify": "false",
  "components[]": [
    "string"
  ],
  "statuses[]": [
    {}
  ],
  "duration": "120",
  "autoStart": "false",
  "autoEnd": "false"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instatus/latest/actions/update-maintenance', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "maintenanceId": "string",
    "message": "string",
    "start": "string",
    "end": "string",
    "status": "string",
    "notify": "false",
    "components[]": ["string"],
    "statuses[]": [{}],
    "duration": "120",
    "autoStart": "false",
    "autoEnd": "false"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Maintenance name. |
| `pageId` | string | yes | Instatus status page ID. |
| `maintenanceId` | string | yes | Instatus maintenance ID. |
| `message` | string | yes | Message for the maintenance update. |
| `start` | string | yes | Maintenance start date and time. |
| `end` | string | yes | Maintenance end date and time. |
| `status` | string | yes | Maintenance status. |
| `notify` | boolean | yes | Whether to notify subscribers. Default: `false`. |
| `components[]` | array<string> | yes | Affected component IDs. Accepts multiple values as an array. |
| `statuses[]` | array<object> | yes | Statuses for each affected component. Include matching component IDs in Component IDs. Accepts multiple values as an array. |
| `duration` | number | yes | Maintenance duration in minutes. Default: `120`. |
| `autoStart` | boolean | yes | Whether Instatus should automatically start the maintenance at the start time. Default: `false`. |
| `autoEnd` | boolean | yes | Whether Instatus should automatically end the maintenance at the end time. Default: `false`. |

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

Through the native Instatus API, this operation is `PUT /v1/:page_id/maintenances/:maintenance_id` (base URL `https://api.instatus.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-maintenance.md) for the provider-specific parameters and requirements.

