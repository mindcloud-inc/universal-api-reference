# Outlign Universal API Examples

These examples use the MindCloud API key and Outlign connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current authenticated user from Outlign.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlign/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outlign/latest/actions/get-current-user?${params}`, {
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
      "avatar": {},
      "avatarUrl": {},
      "capacity": {},
      "colour": "string",
      "createdAt": "string",
      "email": "ava@example.com",
      "emailNotificationFrequency": "ava@example.com",
      "emailVerifiedAt": {},
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "isDemo": true,
      "isGuest": 1,
      "lastName": "Chen",
      "position": "string",
      "timezone": "string",
      "twoFactorRecoveryCodes": {},
      "twoFactorSecret": {},
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/outlign/latest/actions/get-current-user).

## Create Client

Creates a new client in Outlign.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/outlign/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "companyId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/outlign/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "companyId": 1
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
      "data": {
        "company": {
          "id": 1,
          "title": "string"
        },
        "createdAt": "string",
        "id": 1,
        "title": "string",
        "updatedAt": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/outlign/latest/actions/create-client).
