# FireHydrant Universal API Examples

These examples use the MindCloud API key and FireHydrant connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Environments

Retrieves environments from FireHydrant.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-environments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/list-environments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": "string",
          "name": "Ava Chen",
          "slug": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "pagination": {
        "count": 1,
        "items": 1,
        "last": 1,
        "page": 1,
        "pages": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [List Environments action reference](actions/list-environments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fireHydrant/latest/actions/list-environments).

## Create Incident

Creates a new incident in FireHydrant.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/create-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fireHydrant/latest/actions/create-incident', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

Example response:

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

See the full [Create Incident action reference](actions/create-incident.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fireHydrant/latest/actions/create-incident).
