# LogMeIn: Create Incident

Creates a new incident in LogMeIn.

```
POST https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/create-incident
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/create-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "serviceId": "string",
  "summary": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/create-incident', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "serviceId": "string",
    "summary": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Incident title. |
| `serviceId` | string | yes | Service identifier for the incident. |
| `priorityId` | string | no | Priority identifier. |
| `summary` | string | yes | Incident summary. |
| `dueDate` | date | no | Incident due date/time. |
| `assignedUserId` | string | no | Assigned user ID. |
| `categoryId` | string | no | Category ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenantUuid` | string | no | Tenant UUID for the incident. |
| `tagIds[]` | array<string> | no | Tag IDs to attach to the incident. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "priority": "string",
      "referenceNum": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `priority` | string |  |
| `referenceNum` | string |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native LogMeIn API, this operation is `POST /goto-resolve-ticketing/v1/incidents` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-incident.md) for the provider-specific parameters and requirements.

