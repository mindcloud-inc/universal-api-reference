# Solace PubSub+: Get Maintenance Schedules

Retrieves maintenance schedules from Solace PubSub+.

```
GET https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-maintenance-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Solace PubSub+ `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-maintenance-schedules?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-maintenance-schedules?${params}`, {
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

Through the native Solace PubSub+ API, this operation is `GET /api/v2/missionControl/maintenanceSchedules` (base URL `https://api.solace.cloud`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-maintenance-schedules.md) for the provider-specific parameters and requirements.

