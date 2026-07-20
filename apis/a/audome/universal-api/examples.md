# Audome Universal API Examples

These examples use the MindCloud API key and Audome connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Projects

Retrieves project records from Audome.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/audome/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/audome/latest/actions/list-projects?${params}`, {
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

See the full [List Projects action reference](actions/list-projects.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/audome/latest/actions/list-projects).

## Create Client Project



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/audome/latest/actions/create-client-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerName": "Test",
  "title": "MindCloud Client Project Validation"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/audome/latest/actions/create-client-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerName": "Test",
    "title": "MindCloud Client Project Validation"
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

See the full [Create Client Project action reference](actions/create-client-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/audome/latest/actions/create-client-project).
