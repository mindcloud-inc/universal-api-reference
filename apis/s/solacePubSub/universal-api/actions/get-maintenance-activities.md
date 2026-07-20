# Solace PubSub+: Get Maintenance Activities

Retrieves maintenance activities from Solace PubSub+.

```
GET https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-maintenance-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Solace PubSub+ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-maintenance-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-maintenance-activities?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Solace PubSub+ API, this operation is `GET /api/v2/missionControl/maintenanceActivities` (base URL `https://api.solace.cloud`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-maintenance-activities.md) for the provider-specific parameters and requirements.

