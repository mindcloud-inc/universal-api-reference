# Edusign: Create Event

Creates a new event in Edusign.

```
POST https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "start": "string",
  "end": "string",
  "apiId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "start": "string",
    "end": "string",
    "apiId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `apiIdMode` | string | no | Switch between internal IDs and external API IDs for students/professors <br><strong style="color:gold">Important:</strong> When enabled, use external API IDs in the students and professors arrays instead of internal Edusign IDs. |
| `name` | string | yes | Event title (required) |
| `description` | string | no | Detailed description of the event (optional) |
| `start` | string | yes | Event start date and time (required, format: ISO 8601, e.g., "2020-01-20T15:00:00.000Z") |
| `end` | string | yes | Event end date and time (required, format: ISO 8601, e.g., "2020-01-20T18:00:00.000Z") |
| `professors[]` | array<string> | no |  |
| `students[]` | array<string> | no |  |
| `classroom` | string | no | Classroom or location name (will be automatically created if it doesn't exist) |
| `apiId` | string | yes | External API identifier for this event (required for tracking and updates) |
| `apiType` | string | no | Source system or category for the external API (e.g., "calendar_system") |
| `color` | string | no | Display color for the event in hex format (e.g., "#4c00ff") |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "id": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `result.id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `POST /v1/events` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event.md) for the provider-specific parameters and requirements.

