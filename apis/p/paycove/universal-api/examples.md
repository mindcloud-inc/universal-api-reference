# Paycove Universal API Examples

These examples use the MindCloud API key and Paycove connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Paycove.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paycove/latest/actions/get-current-user?${params}`, {
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
      "account": {
        "uniqueId": "string"
      },
      "accountId": 1,
      "createdAt": "string",
      "deletedAt": {},
      "email": "ava@example.com",
      "id": 1,
      "isAdmin": 1,
      "logins": 1,
      "name": "Ava Chen",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/paycove/latest/actions/get-current-user).

## Create Account

Creates an account in Paycove.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "countryCode": "string",
  "currency": "string",
  "legalAcceptanceToken": "string",
  "name": "Ava Chen",
  "timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paycove/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "countryCode": "string",
    "currency": "string",
    "legalAcceptanceToken": "string",
    "name": "Ava Chen",
    "timezone": "string"
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

See the full [Create Account action reference](actions/create-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/paycove/latest/actions/create-account).
