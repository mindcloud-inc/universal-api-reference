# Ecotrak Universal API Examples

These examples use the MindCloud API key and Ecotrak connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User

Retrieves a user from Ecotrak.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecotrak/latest/actions/get-user?connectionId=$CONNECTION_ID&userId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ecotrak/latest/actions/get-user?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ecotrak/latest/actions/get-user).

## Create User

Creates a new user in Ecotrak.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ecotrak/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen",
  "jobTitleId": 1,
  "ssoUser": true,
  "timezone": "string",
  "nteLimit": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ecotrak/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "email": "ava@example.com",
    "firstName": "Ava",
    "lastName": "Chen",
    "jobTitleId": 1,
    "ssoUser": true,
    "timezone": "string",
    "nteLimit": 1
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

See the full [Create User action reference](actions/create-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ecotrak/latest/actions/create-user).
