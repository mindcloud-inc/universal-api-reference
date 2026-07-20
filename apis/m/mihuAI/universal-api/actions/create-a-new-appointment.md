# Mihu AI: Create a New Appointment



```
POST https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/create-a-new-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mihu AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/create-a-new-appointment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endTime": "string",
  "scheduleUuid": "string",
  "startTime": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/create-a-new-appointment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endTime": "string",
    "scheduleUuid": "string",
    "startTime": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactUuid` | string | no |  |
| `description` | string | no |  |
| `endTime` | string | yes |  |
| `notes` | string | no |  |
| `scheduleUuid` | string | yes |  |
| `startTime` | string | yes |  |
| `status` | string | no |  |
| `title` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contactUuid": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endTime": "2026-05-07T12:00:00.000Z",
      "notes": "string",
      "scheduleUuid": "string",
      "startTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contactUuid` | string |  |
| `createdAt` | date |  |
| `description` | string |  |
| `endTime` | date |  |
| `notes` | string |  |
| `scheduleUuid` | string |  |
| `startTime` | date |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Mihu AI API, this operation is `POST /api/v1/appointments` (base URL `https://{{credentials.subdomain}}.mindhunters.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-new-appointment.md) for the provider-specific parameters and requirements.

