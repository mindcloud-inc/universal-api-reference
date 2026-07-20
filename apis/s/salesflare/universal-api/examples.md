# Salesflare Universal API Examples

These examples use the MindCloud API key and Salesflare connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/get-current-user?${params}`, {
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
      "creationDate": "2026-05-07T12:00:00.000Z",
      "dataSources": [
        {}
      ],
      "disabled": true,
      "domain": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "flags": [
        {}
      ],
      "id": 1,
      "intercomHash": "string",
      "isAdmin": true,
      "language": "string",
      "lastname": "Chen",
      "modificationDate": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "picture": "string",
      "role": {},
      "syncStatus": "string",
      "team": {},
      "trialExpired": true,
      "trialExpiryDate": "2026-05-07T12:00:00.000Z",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesflare/latest/actions/get-current-user).

## Create Account



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesflare/latest/actions/create-account', {
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
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Account action reference](actions/create-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/salesflare/latest/actions/create-account).
