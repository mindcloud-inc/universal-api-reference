# Dart Universal API Examples

These examples use the MindCloud API key and Dart connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Space Configuration

Retrieves user space configuration details from Dart.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dart/latest/actions/get-user-space-configuration?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dart/latest/actions/get-user-space-configuration?${params}`, {
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
      "assignees": [
        {
          "email": "ava@example.com",
          "name": "Ava Chen"
        }
      ],
      "dartboards": [
        "string"
      ],
      "folders": [
        "string"
      ],
      "priorities": [
        "string"
      ],
      "sizes": [
        "string"
      ],
      "skills": [
        "string"
      ],
      "statuses": [
        "string"
      ],
      "tags": [
        "string"
      ],
      "today": "2026-05-07T12:00:00.000Z",
      "types": [
        "string"
      ],
      "user": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get User Space Configuration action reference](actions/get-user-space-configuration.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dart/latest/actions/get-user-space-configuration).

## Add Task Attachment From Url

Adds a URL attachment to a Dart task.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dart/latest/actions/add-task-attachment-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dart/latest/actions/add-task-attachment-from-url', {
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
      "kind": "string",
      "name": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Task Attachment From Url action reference](actions/add-task-attachment-from-url.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dart/latest/actions/add-task-attachment-from-url).
