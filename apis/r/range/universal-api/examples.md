# Range Universal API Examples

These examples use the MindCloud API key and Range connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Auth User

Retrieve the authenticated user and active organization session details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/range/latest/actions/get-auth-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/range/latest/actions/get-auth-user?${params}`, {
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
      "accessToken": "string",
      "cues": {},
      "intercomUserHash": "string",
      "loginExpiresAt": "string",
      "org": {},
      "permissions": {},
      "sessionExpiresAt": "string",
      "sessionMaxAge": 1,
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Auth User action reference](actions/get-auth-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/range/latest/actions/get-auth-user).

## Create Team

Create a new team with optional parent and mascot.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/range/latest/actions/create-team" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/range/latest/actions/create-team', {
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
      "archivedAt": "string",
      "createdAt": "string",
      "description": "string",
      "linkHref1": "https://example.com",
      "linkHref2": "https://example.com",
      "linkHref3": "https://example.com",
      "linkText1": "https://example.com",
      "linkText2": "https://example.com",
      "linkText3": "https://example.com",
      "mascot": "string",
      "memberPolicy": "string",
      "name": "Ava Chen",
      "onboardedAt": "string",
      "orgId": "string",
      "parentId": "string",
      "promptsState": "string",
      "relations": [
        {}
      ],
      "slug": "string",
      "teamId": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Team action reference](actions/create-team.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/range/latest/actions/create-team).
