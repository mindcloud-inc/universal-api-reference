# Testomato Universal API Examples

These examples use the MindCloud API key and Testomato connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify API token

Verifies an API token in Testomato.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/verify-api-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testomato/latest/actions/verify-api-token?${params}`, {
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
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Verify API token action reference](actions/verify-api-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/testomato/latest/actions/verify-api-token).

## Add user to project

Adds a user to a Testomato project.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/add-user-to-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "email": "ava@example.com",
  "role": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testomato/latest/actions/add-user-to-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "email": "ava@example.com",
    "role": 1
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
      "canBeRemoved": true,
      "confirmed": true,
      "email": "ava@example.com",
      "id": 1,
      "isPayer": true,
      "notificationDelay": 1,
      "reportPeriod": "string",
      "role": {},
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add user to project action reference](actions/add-user-to-project.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/testomato/latest/actions/add-user-to-project).
