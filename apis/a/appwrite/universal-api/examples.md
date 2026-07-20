# Appwrite Universal API Examples

These examples use the MindCloud API key and Appwrite connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List users

Retrieves a list of users from your Appwrite project.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-list?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/users-list?${params}`, {
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
      "total": 1,
      "users": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List users action reference](actions/users-list.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/appwrite/latest/actions/users-list).

## Create account

Creates a new account in your Appwrite project.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "string",
  "email": "ava@example.com",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/account-create', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "string",
    "email": "ava@example.com",
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
      "$createdAt": "string",
      "$id": "string",
      "$updatedAt": "string",
      "accessedAt": "string",
      "email": "ava@example.com",
      "emailVerification": true,
      "hash": "string",
      "hashOptions": {},
      "labels": [
        "string"
      ],
      "mfa": true,
      "name": "Ava Chen",
      "password": "string",
      "passwordUpdate": "string",
      "phone": "string",
      "phoneVerification": true,
      "prefs": {},
      "registration": "string",
      "status": true,
      "targets": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create account action reference](actions/account-create.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/appwrite/latest/actions/account-create).
