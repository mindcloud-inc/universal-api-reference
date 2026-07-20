# Mihu AI: Create a New Appointment Request



```
POST https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/create-a-new-appointment-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mihu AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/create-a-new-appointment-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scheduleUuid": "string",
  "startTime": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/create-a-new-appointment-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
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
| `contactEmail` | string | no |  |
| `contactName` | string | no |  |
| `contactPhone` | string | no |  |
| `contactSurname` | string | no |  |
| `contactUuid` | string | no |  |
| `description` | string | no |  |
| `endTime` | string | no |  |
| `notes` | string | no |  |
| `scheduleUuid` | string | yes |  |
| `startTime` | string | yes |  |
| `title` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appointment": {},
      "approvalNote": "string",
      "approvedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endTime": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "notes": "string",
      "rejectedAt": "2026-05-07T12:00:00.000Z",
      "rejectionReason": "string",
      "startTime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "title": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appointment` | object |  |
| `approvalNote` | string |  |
| `approvedAt` | date |  |
| `description` | string |  |
| `endTime` | date |  |
| `id` | number |  |
| `notes` | string |  |
| `rejectedAt` | date |  |
| `rejectionReason` | string |  |
| `startTime` | date |  |
| `status` | string |  |
| `title` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Mihu AI API, this operation is `POST /api/v1/appointment-requests` (base URL `https://{{credentials.subdomain}}.mindhunters.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-new-appointment-request.md) for the provider-specific parameters and requirements.

