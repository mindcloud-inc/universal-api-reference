# Superthread Universal API Examples

These examples use the MindCloud API key and Superthread connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Account



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superthread/latest/actions/get-my-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superthread/latest/actions/get-my-account?${params}`, {
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
      "token_outdated": true,
      "token_privileged": true,
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Get My Account action reference](actions/get-my-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/superthread/latest/actions/get-my-account).

## Add Member to Space



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superthread/latest/actions/add-member-to-space" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "projectId": "string",
  "members[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superthread/latest/actions/add-member-to-space', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "projectId": "string",
    "members[]": [{}]
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

See the full [Add Member to Space action reference](actions/add-member-to-space.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/superthread/latest/actions/add-member-to-space).
