# Documentum Universal API Examples

These examples use the MindCloud API key and Documentum connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Repositories



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-repositories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documentum/latest/actions/list-repositories?${params}`, {
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
      "entries": [
        {}
      ],
      "id": "string",
      "links": [
        {}
      ],
      "title": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Repositories action reference](actions/list-repositories.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/documentum/latest/actions/list-repositories).

## Apply Lifecycle State



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/documentum/latest/actions/apply-lifecycle-state" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "repositoryName": "d2repo",
  "properties": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documentum/latest/actions/apply-lifecycle-state', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "repositoryName": "d2repo",
    "properties": "[object Object]"
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
      "entries": [
        {
          "id": "string",
          "message": "string",
          "status": "string"
        }
      ],
      "id": "string",
      "message": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Apply Lifecycle State action reference](actions/apply-lifecycle-state.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/documentum/latest/actions/apply-lifecycle-state).
