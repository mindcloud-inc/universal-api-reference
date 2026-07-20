# Samply Universal API Examples

These examples use the MindCloud API key and Samply connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samply/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samply/latest/actions/list-projects?${params}`, {
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
      "artwork": "string",
      "color": "string",
      "creator": {},
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "size": 1,
      "sortBy": {},
      "timeCreated": 1,
      "timeModified": 1
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/samply/latest/actions/list-projects).

## Add Items To Folder



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/samply/latest/actions/add-items-to-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/samply/latest/actions/add-items-to-folder', {
  method: 'PUT',
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
      "children": [
        {}
      ],
      "color": "string",
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "timeCreated": 1,
      "trashed": true
    }
  ],
  "meta": {}
}
```

See the full [Add Items To Folder action reference](actions/add-items-to-folder.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/samply/latest/actions/add-items-to-folder).
