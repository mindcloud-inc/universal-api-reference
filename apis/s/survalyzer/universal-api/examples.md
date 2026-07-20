# Survalyzer Universal API Examples

These examples use the MindCloud API key and Survalyzer connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Workspaces



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/list-workspaces?${params}`, {
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
      "errorCode": "string",
      "errorMessage": "string",
      "isSuccess": true,
      "totalCount": 1,
      "workspaces": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Workspaces action reference](actions/list-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/survalyzer/latest/actions/list-workspaces).

## Create And Invite Members



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/create-and-invite-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/survalyzer/latest/actions/create-and-invite-members', {
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
      "errorCode": "string",
      "errorMessage": "string",
      "isSuccess": true
    }
  ],
  "meta": {}
}
```

See the full [Create And Invite Members action reference](actions/create-and-invite-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/survalyzer/latest/actions/create-and-invite-members).
