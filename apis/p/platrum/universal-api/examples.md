# Platrum Universal API Examples

These examples use the MindCloud API key and Platrum connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List profiles

Retrieves profiles from Platrum.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/platrum/latest/actions/list-profiles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/platrum/latest/actions/list-profiles?${params}`, {
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [List profiles action reference](actions/list-profiles.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/platrum/latest/actions/list-profiles).

## Create task

Creates a new task in Platrum.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/platrum/latest/actions/create-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/platrum/latest/actions/create-task', {
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
      "data": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create task action reference](actions/create-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/platrum/latest/actions/create-task).
