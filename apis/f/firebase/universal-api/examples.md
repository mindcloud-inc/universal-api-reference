# Firebase Universal API Examples

These examples use the MindCloud API key and Firebase connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Firebase Projects

Retrieves Firebase projects.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/list-firebase-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/firebase/latest/actions/list-firebase-projects?${params}`, {
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
      "annotations": {},
      "displayName": "Ava Chen",
      "etag": "string",
      "name": "Ava Chen",
      "projectId": "string",
      "projectNumber": "string",
      "resources": {},
      "state": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Firebase Projects action reference](actions/list-firebase-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/firebase/latest/actions/list-firebase-projects).

## Add Firebase To Project

Adds Firebase to a Google Cloud project.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/add-firebase-to-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/firebase/latest/actions/add-firebase-to-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string"
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
      "done": true,
      "error": {},
      "metadata": {},
      "name": "Ava Chen",
      "response": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Firebase To Project action reference](actions/add-firebase-to-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/firebase/latest/actions/add-firebase-to-project).
