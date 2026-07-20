# Kameleoon Universal API Examples

These examples use the MindCloud API key and Kameleoon connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get all accounts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-accounts?connectionId=$CONNECTION_ID&paramsIo=page%3D1%2C%20perPage%3D20" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "paramsIo": "page=1, perPage=20"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/get-all-accounts?${params}`, {
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "isPasswordExpired": true,
      "isProductRecoAllowed": true,
      "lastName": "Chen",
      "passwordBlocked": true,
      "preferredLocale": "string",
      "roles": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get all accounts action reference](actions/get-all-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kameleoon/latest/actions/get-all-accounts).

## Create account



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "firstName": "Ava",
  "lastName": "Chen",
  "password": "string",
  "passwordConfirm": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kameleoon/latest/actions/create-account', {
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
    "password": "string",
    "passwordConfirm": "string"
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "isPasswordExpired": true,
      "isProductRecoAllowed": true,
      "lastName": "Chen",
      "passwordBlocked": true,
      "preferredLocale": "string",
      "roles": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create account action reference](actions/create-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/kameleoon/latest/actions/create-account).
