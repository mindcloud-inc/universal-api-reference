# Solace PubSub+: Get Maintenance Activity

Retrieves a maintenance activity from Solace PubSub+.

```
GET https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-maintenance-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Solace PubSub+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-maintenance-activity?connectionId=$CONNECTION_ID&maintenanceActivityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "maintenanceActivityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-maintenance-activity?${params}`, {
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
| `maintenanceActivityId` | string | yes | Maintenance activity identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "endTime": "2026-05-07T12:00:00.000Z",
      "environmentId": "string",
      "id": "string",
      "maintenanceType": "string",
      "maintenanceWindowId": "string",
      "orgId": "string",
      "resourceId": "string",
      "resourceName": "Ava Chen",
      "resourceType": "string",
      "scheduledEndTime": "2026-05-07T12:00:00.000Z",
      "scheduledStartTime": "2026-05-07T12:00:00.000Z",
      "startTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `endTime` | date |  |
| `environmentId` | string |  |
| `id` | string |  |
| `maintenanceType` | string |  |
| `maintenanceWindowId` | string |  |
| `orgId` | string |  |
| `resourceId` | string |  |
| `resourceName` | string |  |
| `resourceType` | string |  |
| `scheduledEndTime` | date |  |
| `scheduledStartTime` | date |  |
| `startTime` | date |  |

## Native endpoint

Through the native Solace PubSub+ API, this operation is `GET /api/v2/missionControl/maintenanceActivities/{maintenanceActivityId}` (base URL `https://api.solace.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-maintenance-activity.md) for the provider-specific parameters and requirements.

