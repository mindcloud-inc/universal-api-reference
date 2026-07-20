# LastPass Universal API Examples

These examples use the MindCloud API key and LastPass connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Detailed Shared Folder Data

Retrieves detailed shared folder data from LastPass.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/get-detailed-shared-folder-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/get-detailed-shared-folder-data?${params}`, {
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
      "give": true,
      "groups": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "readonly": true,
      "sites": [
        {}
      ],
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Get Detailed Shared Folder Data action reference](actions/get-detailed-shared-folder-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lastPass/latest/actions/get-detailed-shared-folder-data).

## Create User

Creates a new user in LastPass.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lastPass/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen",
    "password": "string"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create User action reference](actions/create-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lastPass/latest/actions/create-user).
