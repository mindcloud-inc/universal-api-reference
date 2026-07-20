# Mihu AI: Get a Specific Appointment Request



```
GET https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-a-specific-appointment-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mihu AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-a-specific-appointment-request?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mihuAI/latest/actions/get-a-specific-appointment-request?${params}`, {
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
| `uuid` | string | yes |  |

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

Through the native Mihu AI API, this operation is `GET /api/v1/appointment-requests/:uuid` (base URL `https://{{credentials.subdomain}}.mindhunters.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-specific-appointment-request.md) for the provider-specific parameters and requirements.

