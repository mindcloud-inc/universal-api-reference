# Svix Universal API Examples

These examples use the MindCloud API key and Svix connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Applications

Retrieves applications from Svix.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/svix/latest/actions/list-applications?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/svix/latest/actions/list-applications?${params}`, {
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
      "data": [
        {}
      ],
      "done": true,
      "iterator": "string",
      "prevIterator": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Applications action reference](actions/list-applications.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/svix/latest/actions/list-applications).

## Aggregate App Stats

Starts background aggregation of Svix application statistics.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/svix/latest/actions/aggregate-app-stats" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/svix/latest/actions/aggregate-app-stats', {
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
      "id": "string",
      "status": "string",
      "task": "string",
      "unresolvedAppIds": [
        "string"
      ],
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Aggregate App Stats action reference](actions/aggregate-app-stats.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/svix/latest/actions/aggregate-app-stats).
