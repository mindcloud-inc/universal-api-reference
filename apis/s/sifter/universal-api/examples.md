# Sifter Universal API Examples

These examples use the MindCloud API key and Sifter connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves accessible open projects from Sifter.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sifter/latest/actions/list-projects?${params}`, {
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
      "apiCategoriesUrl": "https://example.com",
      "apiIssuesUrl": "https://example.com",
      "apiMilestonesUrl": "https://example.com",
      "apiNewIssueEmailAddress": "ava@example.com",
      "apiPeopleUrl": "https://example.com",
      "apiUrl": "https://example.com",
      "archived": true,
      "issuesUrl": "https://example.com",
      "milestonesUrl": "https://example.com",
      "name": "Ava Chen",
      "primaryCompanyName": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sifter/latest/actions/list-projects).

## Create Comment

Creates a new comment on a Sifter issue.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sifter/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string",
  "issueId": 1,
  "projectId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sifter/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string",
    "issueId": 1,
    "projectId": 1
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
      "assigneeEmail": "ava@example.com",
      "assigneeName": "Ava Chen",
      "attachments": [
        {}
      ],
      "body": "string",
      "category": "string",
      "commenter": "string",
      "commenterEmail": "ava@example.com",
      "createdAt": "string",
      "internal": true,
      "milestoneName": "Ava Chen",
      "opener": "string",
      "openerEmail": "ava@example.com",
      "priority": "string",
      "project": "string",
      "status": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Comment action reference](actions/create-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sifter/latest/actions/create-comment).
