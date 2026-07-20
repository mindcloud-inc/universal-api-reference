# Supabugs Universal API Examples

These examples use the MindCloud API key and Supabugs connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Project

Retrieves current project details from Supabugs.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/get-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/get-project?${params}`, {
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
      "archived": true,
      "clientCompanyName": "Ava Chen",
      "closedIssuesCount": 1,
      "code": "string",
      "contractNumber": "string",
      "description": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "issuesCount": 1,
      "name": "Ava Chen",
      "openIssuesCount": 1,
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Project action reference](actions/get-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/supabugs/latest/actions/get-project).

## Add Issue Comment

Creates a new comment on a Supabugs issue.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/add-issue-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/supabugs/latest/actions/add-issue-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "content": "string"
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
      "accountId": "string",
      "assignees": [
        {}
      ],
      "attachments": [
        {}
      ],
      "closed": true,
      "closedAt": "2026-05-07T12:00:00.000Z",
      "code": "string",
      "comments": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdById": "string",
      "createdByUser": {},
      "description": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "environment": {},
      "history": [
        {}
      ],
      "id": "string",
      "issuedId": "string",
      "issuedType": "string",
      "priority": {},
      "priorityId": "string",
      "project": {},
      "projectId": "string",
      "publicShareLink": "https://example.com",
      "relatedToIssue": "string",
      "relatedToIssueId": "string",
      "severity": {},
      "severityId": "string",
      "status": {},
      "statusId": "string",
      "title": "string",
      "type": {},
      "typeId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedById": "string",
      "updatedByUser": {},
      "watchers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add Issue Comment action reference](actions/add-issue-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/supabugs/latest/actions/add-issue-comment).
