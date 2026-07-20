# Insightful Universal API Examples

These examples use the MindCloud API key and Insightful connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Teams

Retrieves teams from your Insightful account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/insightful/latest/actions/list-teams?${params}`, {
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
      "default": true,
      "description": "string",
      "id": "string",
      "ignoreNeutral": true,
      "ignoreProductive": true,
      "ignoreUnproductive": true,
      "ignoreUnreviewed": true,
      "modelName": "Ava Chen",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Teams action reference](actions/list-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/insightful/latest/actions/list-teams).

## Create Project

Creates a new project in your Insightful account.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/insightful/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employees[]": [
    "string"
  ],
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightful/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "employees[]": ["string"],
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
      "archived": true,
      "billable": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "description": "string",
      "employees": [
        "string"
      ],
      "id": "string",
      "modelName": "Ava Chen",
      "name": "Ava Chen",
      "organizationId": "string",
      "payroll": {
        "billRate": 1,
        "overtimeBillRate": 1
      },
      "priorities": [
        "string"
      ],
      "screenshotSettings": {
        "screenshotEnabled": true
      },
      "statuses": [
        "string"
      ],
      "teams": [
        "string"
      ],
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create Project action reference](actions/create-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/insightful/latest/actions/create-project).
