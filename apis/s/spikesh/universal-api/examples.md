# Spike.sh Universal API Examples

These examples use the MindCloud API key and Spike.sh connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Users

Retrieves all users in your Spike.sh organization.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spikesh/latest/actions/get-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spikesh/latest/actions/get-users?${params}`, {
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

See the full [Get Users action reference](actions/get-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spikesh/latest/actions/get-users).

## Create Service

Creates a new service in Spike.sh.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/spikesh/latest/actions/create-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "teamId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/spikesh/latest/actions/create-service', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "teamId": "string"
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

See the full [Create Service action reference](actions/create-service.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/spikesh/latest/actions/create-service).
