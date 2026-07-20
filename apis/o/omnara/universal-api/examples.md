# Omnara Universal API Examples

These examples use the MindCloud API key and Omnara connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User Profile



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-current-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/omnara/latest/actions/get-current-user-profile?${params}`, {
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
      "createdAt": "string",
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User Profile action reference](actions/get-current-user-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/omnara/latest/actions/get-current-user-profile).

## Create PAT



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/omnara/latest/actions/create-pat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/omnara/latest/actions/create-pat', {
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
      "createdAt": "string",
      "id": "string",
      "lastUsedAt": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create PAT action reference](actions/create-pat.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/omnara/latest/actions/create-pat).
