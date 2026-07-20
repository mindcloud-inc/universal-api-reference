# Solace PubSub+: Get Maintenance Schedule

Retrieves a maintenance schedule from Solace PubSub+.

```
GET https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-maintenance-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Solace PubSub+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-maintenance-schedule?connectionId=$CONNECTION_ID&maintenanceScheduleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "maintenanceScheduleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-maintenance-schedule?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `maintenanceScheduleId` | string | yes | Maintenance schedule identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdBy": "string",
      "createdTime": "2026-05-07T12:00:00.000Z",
      "environmentId": "string",
      "id": "string",
      "maintenanceType": "string",
      "organizationId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string |  |
| `createdTime` | date |  |
| `environmentId` | string |  |
| `id` | string |  |
| `maintenanceType` | string |  |
| `organizationId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Solace PubSub+ API, this operation is `GET /api/v2/missionControl/maintenanceSchedules/{maintenanceScheduleId}` (base URL `https://api.solace.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-maintenance-schedule.md) for the provider-specific parameters and requirements.

