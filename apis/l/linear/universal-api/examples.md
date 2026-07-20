# Linear Universal API Examples

These examples use the MindCloud API key and Linear connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Teams

Retrieves teams from Linear.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linear/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linear/latest/actions/list-teams?${params}`, {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Teams action reference](actions/list-teams.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linear/latest/actions/list-teams).

## Create Issue

Create Linear Issue.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linear/latest/actions/create-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linear/latest/actions/create-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "activitySummary": {},
      "addedToCycleAt": {},
      "addedToProjectAt": "string",
      "addedToTeamAt": "string",
      "archivedAt": {},
      "autoArchivedAt": {},
      "autoClosedAt": {},
      "boardOrder": 1,
      "branchName": "Ava Chen",
      "canceledAt": {},
      "completedAt": {},
      "createdAt": "string",
      "customerTicketCount": 1,
      "description": "string",
      "dueDate": {},
      "estimate": {},
      "id": "string",
      "identifier": "string",
      "integrationSourceType": {},
      "number": 1,
      "priority": 1,
      "priorityLabel": "string",
      "prioritySortOrder": 1,
      "slaBreachesAt": {},
      "slaHighRiskAt": {},
      "slaMediumRiskAt": {},
      "slaStartedAt": {},
      "slaType": "string",
      "startedAt": {},
      "startedTriageAt": {},
      "subIssueSortOrder": {},
      "suggestionsGeneratedAt": {},
      "title": "string",
      "trashed": {},
      "triagedAt": {},
      "updatedAt": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Issue action reference](actions/create-issue.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linear/latest/actions/create-issue).
