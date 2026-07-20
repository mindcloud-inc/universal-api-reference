# Sumo Logic: List Health Events

Retrieves unresolved health events from your Sumo Logic account.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-health-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-health-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-health-events?${params}`, {
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
      "details": {
        "description": "string",
        "error": "string",
        "trackerId": "string"
      },
      "eventId": "string",
      "eventName": "Ava Chen",
      "eventTime": "2026-05-07T12:00:00.000Z",
      "resourceIdentity": {
        "id": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "severityLevel": "string",
      "subsystem": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details.description` | string |  |
| `details.error` | string |  |
| `details.trackerId` | string |  |
| `eventId` | string |  |
| `eventName` | string |  |
| `eventTime` | date |  |
| `resourceIdentity.id` | string |  |
| `resourceIdentity.name` | string |  |
| `resourceIdentity.type` | string |  |
| `severityLevel` | string |  |
| `subsystem` | string |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v1/healthEvents` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-health-events.md) for the provider-specific parameters and requirements.

