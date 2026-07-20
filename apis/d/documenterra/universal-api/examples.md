# Documenterra Universal API Examples

These examples use the MindCloud API key and Documenterra connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves projects and publications from Documenterra.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/list-projects?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/documenterra/latest/actions/list-projects).

## Create Page

Creates a page in Documenterra.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/create-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assigneeUserName": "Ava Chen",
  "id": "string",
  "ownerUserName": "Ava Chen",
  "projectId": "string",
  "statusName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documenterra/latest/actions/create-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assigneeUserName": "Ava Chen",
    "id": "string",
    "ownerUserName": "Ava Chen",
    "projectId": "string",
    "statusName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Page action reference](actions/create-page.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/documenterra/latest/actions/create-page).
