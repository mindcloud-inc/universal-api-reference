# DogQ Universal API Examples

These examples use the MindCloud API key and DogQ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Run Project

Runs a DogQ project with optional variables and contexts.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dogQ/latest/actions/run-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dogQ/latest/actions/run-project', {
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Run Project action reference](actions/run-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dogQ/latest/actions/run-project).
