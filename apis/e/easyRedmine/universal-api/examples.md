# Easy Redmine Universal API Examples

These examples use the MindCloud API key and Easy Redmine connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects from Easy Redmine.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/list-projects?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/list-projects?${params}`, {
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
      "createdOn": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "identifier": "string",
      "name": "Ava Chen",
      "status": 1,
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyRedmine/latest/actions/list-projects).

## Add Issue To Favorites

Adds an issue to favorites in Easy Redmine.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/add-issue-to-favorites" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyRedmine/latest/actions/add-issue-to-favorites', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
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
      "id": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Issue To Favorites action reference](actions/add-issue-to-favorites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyRedmine/latest/actions/add-issue-to-favorites).
