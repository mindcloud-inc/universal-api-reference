# Worksection Universal API Examples

These examples use the MindCloud API key and Worksection connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worksection/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worksection/latest/actions/list-projects?${params}`, {
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
      "company": "string",
      "dateAdded": "string",
      "id": "string",
      "name": "Ava Chen",
      "page": "string",
      "status": "string",
      "userFrom": {},
      "userTo": {}
    }
  ],
  "meta": {}
}
```

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/worksection/latest/actions/list-projects).

## Activate Project



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/worksection/latest/actions/activate-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/worksection/latest/actions/activate-project', {
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
      "company": "string",
      "dateAdded": "string",
      "id": "string",
      "name": "Ava Chen",
      "page": "string",
      "status": "string",
      "userFrom": {},
      "userTo": {}
    }
  ],
  "meta": {}
}
```

See the full [Activate Project action reference](actions/activate-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/worksection/latest/actions/activate-project).
