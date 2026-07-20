# DecisionVault: Get Event

Retrieves an event from DecisionVault by ID.

```
GET https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DecisionVault `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/get-event?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/decisionVault/latest/actions/get-event?${params}`, {
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
| `eventId` | string | yes | The event ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event_id": "string",
      "event_type": "string",
      "matter": {},
      "meta": {},
      "occured_at": "2026-05-07T12:00:00.000Z",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event_id` | string |  |
| `event_type` | string |  |
| `matter` | object |  |
| `meta` | object |  |
| `occured_at` | date |  |
| `user` | object |  |

## Native endpoint

Through the native DecisionVault API, this operation is `GET /events/:event_id` (base URL `https://api.decisionvault.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

