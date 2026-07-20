# Userback Universal API Examples

These examples use the MindCloud API key and Userback connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Lists the projects available in Userback.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userback/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userback/latest/actions/list-projects?${params}`, {
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
      "created": "string",
      "createdBy": 1,
      "id": 1,
      "isArchived": true,
      "name": "Ava Chen",
      "projectType": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/userback/latest/actions/list-projects).

## Create Feedback

Creates a new feedback item in Userback.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userback/latest/actions/create-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "137605",
  "feedbackType": "General",
  "title": "App feedback from MindCloud"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userback/latest/actions/create-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "137605",
    "feedbackType": "General",
    "title": "App feedback from MindCloud"
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
      "allowPublicComment": true,
      "created": "string",
      "description": "string",
      "dueDate": "string",
      "email": "ava@example.com",
      "feedbackType": "string",
      "id": 1,
      "isPinned": true,
      "isPortalApproved": true,
      "isShared": true,
      "modified": "string",
      "name": "Ava Chen",
      "pageUrl": "https://example.com",
      "priority": "string",
      "projectId": 1,
      "rating": "string",
      "session": {
        "colorDepth": 1,
        "dpi": 1,
        "resolutionX": 1,
        "resolutionY": 1,
        "userAgent": "string",
        "windowHeight": 1,
        "windowWidth": 1
      },
      "shareUrl": "https://example.com",
      "title": "string",
      "userIdentification": "string",
      "voteCount": 1,
      "workflow": {
        "color": "string",
        "id": 1,
        "name": "Ava Chen",
        "sort": 1
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Feedback action reference](actions/create-feedback.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/userback/latest/actions/create-feedback).
