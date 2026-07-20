# GitHub Utils Universal API Examples

These examples use the MindCloud API key and GitHub Utils connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User

Retrieves the authenticated user from GitHub.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/get-authenticated-user?${params}`, {
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
      "avatar_url": "https://example.com",
      "bio": "string",
      "blog": "string",
      "company": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "followers": 1,
      "following": 1,
      "html_url": "https://example.com",
      "id": 1,
      "location": "string",
      "login": "string",
      "name": "Ava Chen",
      "node_id": "string",
      "public_repos": 1,
      "type": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gitHubUtils/latest/actions/get-authenticated-user).

## Create Issue

Creates a new issue on GitHub.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/create-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "owner": "string",
  "repo": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gitHubUtils/latest/actions/create-issue', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "owner": "string",
    "repo": "string",
    "title": "string"
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
      "assignee": {},
      "assignees": [
        {}
      ],
      "author_association": "string",
      "body": "string",
      "closed_at": "2026-05-07T12:00:00.000Z",
      "comments": 1,
      "comments_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "events_url": "https://example.com",
      "html_url": "https://example.com",
      "id": 1,
      "labels": [
        {}
      ],
      "labels_url": "https://example.com",
      "locked": true,
      "milestone": {},
      "node_id": "string",
      "number": 1,
      "repository_url": "https://example.com",
      "state": "string",
      "state_reason": "string",
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Issue action reference](actions/create-issue.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gitHubUtils/latest/actions/create-issue).
