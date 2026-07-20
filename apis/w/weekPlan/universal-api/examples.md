# Week Plan Universal API Examples

These examples use the MindCloud API key and Week Plan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Workspaces



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/get-workspaces?${params}`, {
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
      "Description": "string",
      "IsArchived": true,
      "Name": "Ava Chen",
      "StartOfWeek": 1,
      "UserCanAdministrate": true,
      "WorkspaceId": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Workspaces action reference](actions/get-workspaces.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weekPlan/latest/actions/get-workspaces).

## Add User Email



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/add-user-email" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/add-user-email', {
  method: 'PUT',
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
      "Email": "ava@example.com",
      "EmailVerified": true,
      "Message": "string",
      "UserId": 1
    }
  ],
  "meta": {}
}
```

See the full [Add User Email action reference](actions/add-user-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weekPlan/latest/actions/add-user-email).
