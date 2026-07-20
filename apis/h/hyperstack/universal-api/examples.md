# Hyperstack Certificates Universal API Examples

These examples use the MindCloud API key and Hyperstack Certificates connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Authenticate



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/authenticate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/authenticate?${params}`, {
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
      "accountId": "string",
      "accountName": "Ava Chen",
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Authenticate action reference](actions/authenticate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hyperstack/latest/actions/authenticate).

## Create Credential Group



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/create-credential-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "blockchain": true,
  "description": "string",
  "does_expire": true,
  "group_code": "string",
  "tags": {},
  "title": "string",
  "url": "https://example.com",
  "validity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperstack/latest/actions/create-credential-group', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "blockchain": true,
    "description": "string",
    "does_expire": true,
    "group_code": "string",
    "tags": {},
    "title": "string",
    "url": "https://example.com",
    "validity": 1
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
      "group_key": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Credential Group action reference](actions/create-credential-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hyperstack/latest/actions/create-credential-group).
