# FireHydrant: Update Incident

Updates an existing incident in FireHydrant.

```
PUT https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/update-incident
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FireHydrant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/update-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "incidentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/update-incident', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "incidentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `incidentId` | string | yes | The FireHydrant incident ID. |
| `summary` | string | no | Update the incident summary. |
| `description` | string | no | Update the incident description. |
| `severity` | string | no | Update the incident severity. |
| `priority` | string | no | Update the incident priority. |
| `incidentTypeId` | string | no | Update the incident type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "aiIncidentSummary": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "currentMilestone": "string",
      "customerImpactSummary": "string",
      "customersImpacted": 1,
      "description": "string",
      "discardedAt": "2026-05-07T12:00:00.000Z",
      "environments": [
        {}
      ],
      "functionalities": [
        {}
      ],
      "id": "string",
      "impacts": [
        {}
      ],
      "incidentType": {},
      "incidentUrl": "https://example.com",
      "lastNote": {},
      "lastUpdate": "string",
      "name": "Ava Chen",
      "number": 1,
      "organization": {},
      "organizationId": "string",
      "priority": "string",
      "privateId": "string",
      "privateStatusPageUrl": "https://example.com",
      "reportId": "string",
      "roleAssignments": [
        {}
      ],
      "services": [
        {}
      ],
      "severity": "string",
      "severityColor": "string",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "statusPages": [
        {}
      ],
      "summary": "string",
      "tagList": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `aiIncidentSummary` | string |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `currentMilestone` | string |  |
| `customerImpactSummary` | string |  |
| `customersImpacted` | number |  |
| `description` | string |  |
| `discardedAt` | date |  |
| `environments` | array<object> |  |
| `functionalities` | array<object> |  |
| `id` | string |  |
| `impacts` | array<object> |  |
| `incidentType` | object |  |
| `incidentUrl` | string |  |
| `lastNote` | object |  |
| `lastUpdate` | string |  |
| `name` | string |  |
| `number` | number |  |
| `organization` | object |  |
| `organizationId` | string |  |
| `priority` | string |  |
| `privateId` | string |  |
| `privateStatusPageUrl` | string |  |
| `reportId` | string |  |
| `roleAssignments` | array<object> |  |
| `services` | array<object> |  |
| `severity` | string |  |
| `severityColor` | string |  |
| `startedAt` | date |  |
| `statusPages` | array<object> |  |
| `summary` | string |  |
| `tagList` | array<string> |  |

## Native endpoint

Through the native FireHydrant API, this operation is `PATCH /incidents/:incident_id` (base URL `https://api.firehydrant.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-incident.md) for the provider-specific parameters and requirements.

