# AnnounceKit Universal API Examples

These examples use the MindCloud API key and AnnounceKit connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Active Project

Retrieves the active project from AnnounceKit.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/announceKit/latest/actions/get-active-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/announceKit/latest/actions/get-active-project?${params}`, {
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

See the full [Get Active Project action reference](actions/get-active-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/announceKit/latest/actions/get-active-project).

## Create Draft Post

Creates a draft post in AnnounceKit.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/announceKit/latest/actions/create-draft-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "66505",
  "title": "string",
  "body": "string",
  "localeId": "en"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/announceKit/latest/actions/create-draft-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "66505",
    "title": "string",
    "body": "string",
    "localeId": "en"
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
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Draft Post action reference](actions/create-draft-post.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/announceKit/latest/actions/create-draft-post).
