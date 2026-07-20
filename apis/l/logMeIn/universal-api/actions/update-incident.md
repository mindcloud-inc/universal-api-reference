# LogMeIn: Update Incident

Updates an existing incident in LogMeIn.

```
PUT https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/update-incident
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LogMeIn `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/update-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "referenceNum": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logMeIn/latest/actions/update-incident', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "referenceNum": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `referenceNum` | string | yes | Required incident reference number. |
| `title` | string | no | Updated incident title. |
| `summary` | string | no | Updated incident summary. |
| `assignedUserId` | string | no | Updated assigned user ID. |
| `priorityId` | string | no | Updated priority ID. |
| `dueDate` | date | no | Updated due date/time. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tenant.uuid` | string | no | Tenant UUID. |
| `tagIdsToAdd[]` | array<string> | no | Tag IDs to add to the incident. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "priority": "string",
      "referenceNum": "string",
      "status": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `priority` | string |  |
| `referenceNum` | string |  |
| `status` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native LogMeIn API, this operation is `PUT /goto-resolve-ticketing/v1/incidents/:referenceNum` (base URL `https://api.goto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-incident.md) for the provider-specific parameters and requirements.

