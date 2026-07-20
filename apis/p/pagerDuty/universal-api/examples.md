# PagerDuty Universal API Examples

These examples use the MindCloud API key and PagerDuty connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Abilities



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-abilities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-abilities?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Abilities action reference](actions/list-abilities.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pagerDuty/latest/actions/list-abilities).

## Create Incident



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/create-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "incident.title": "string",
  "incident.service.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/create-incident', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "incident.title": "string",
    "incident.service.id": "string"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "escalationPolicy": {
        "id": "string",
        "summary": "string",
        "type": "string"
      },
      "htmlUrl": "https://example.com",
      "id": "string",
      "incidentKey": "string",
      "incidentNumber": 1,
      "priority": {
        "id": "string",
        "summary": "string",
        "type": "string"
      },
      "self": "string",
      "service": {
        "htmlUrl": "https://example.com",
        "id": "string",
        "self": "string",
        "summary": "string",
        "type": "string"
      },
      "status": "string",
      "summary": "string",
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "urgency": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Incident action reference](actions/create-incident.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pagerDuty/latest/actions/create-incident).
