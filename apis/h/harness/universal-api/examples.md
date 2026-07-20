# Harness Universal API Examples

These examples use the MindCloud API key and Harness connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User Info

Retrieves the current user from Harness.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/harness/latest/actions/get-current-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harness/latest/actions/get-current-user-info?${params}`, {
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
      "admin": true,
      "email": "ava@example.com",
      "name": "Ava Chen",
      "username": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User Info action reference](actions/get-current-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/harness/latest/actions/get-current-user-info).

## Create Connector

Creates a new connector in Harness.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harness/latest/actions/create-connector" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "connector.identifier": "string",
  "connector.name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harness/latest/actions/create-connector', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "connector.identifier": "string",
    "connector.name": "Ava Chen"
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
      "connector": {},
      "createdAt": 1,
      "lastModifiedAt": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Connector action reference](actions/create-connector.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/harness/latest/actions/create-connector).
